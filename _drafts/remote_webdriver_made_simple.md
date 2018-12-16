---
layout: post
title: "(DRAFT) RemoteWebdriver made simple"
categories: [draft]
---

## TL;DR:

If you need to quickly do some scraping of "static"-like pages you can setup a system to:
- raise a docker container with firefox+webdriver standalone
- have a maven project that produces an executable jar with your scraping
- run the jar given arguments (getting the webdriver host "dinamically", login data, scrape target data)
- kill the docker container
- extra: put it on a CI Job (example 1: jenkins; example 2: gitlab ci; example 3: travis)

## Raising and killing a container

TBD

```shell
#!/bin/bash

# Raise docker instance with remote browser + webdriver, run tests, kill docker instance
set -x

FF_NAME=default_firefox
java -version
docker version

# Start containers
docker run -d -P --name=$FF_NAME selenium/standalone-firefox
docker ps

HOST=http://$(docker port default_firefox 4444)
echo $HOST

# Run tests
mvn clean install test

# Stop containers
docker stop $(docker ps -a -q --filter "name=$FF_NAME")
docker ps
docker rm $(docker ps -a -f status=exited -q)
```


## Setting up Webdriver dynamically

First, let's set up an interface for our WebDriver that can have multiple implementations (it can be for a remote browser or a local browser):

```java
import org.openqa.selenium.WebDriver;

public interface Driver {
    WebDriver instance();
}
```

Now we can create different implementations for this interface. Let's start with the usual that we can run on our own machine, Chrome:

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.chrome.ChromeOptions;

public class LocalChromeDriver implements Driver {

    private final String driver;

    public LocalChromeDriver(final String driver) {
        this.driver = driver;
    }

    @Override
    public WebDriver instance() {
        System.setProperty("webdriver.chrome.driver", driver);
        final ChromeOptions options = new ChromeOptions();
        options.addArguments("--headless");
        return new ChromeDriver(options);
    }
}
```

Notice how I'm already setting up the `--headless` option. This is optional, you can choose to leave that out.
Notice also the setup of property `webdriver.chrome.driver`. What this means is that later on, when you want to
have an instance of this driver, you'd have to instantiate it with the path for the driver on your machine, that's why
we have the `driver` internal variable to the object. It's the path for the driver. You can download chromedriver to
interact with your local browser [here](https://sites.google.com/a/chromium.org/chromedriver/downloads).

So in the end, to create an instance of the driver, you'd have to do something like this:

```java
final WebDriver driver = new LocalChromeDriver(/*path to chromedriver you downloaded*/).instance();
```

You can also do an implementation for other local browsers if you wish, for example Firefox:

```java
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.firefox.FirefoxOptions;

public class LocalFirefoxDriver implements Driver {

    private final String driver;

    public LocalFirefoxDriver(final String driver) {
        this.driver = driver;
    }

    @Override
    public WebDriver instance() {
        System.setProperty("webdriver.gecko.instance", driver);
        return new FirefoxDriver(new FirefoxOptions().addArguments("-headless"));
    }
}
```

Now, for a remote WebDriver, useful for running your tests/scrapping scripts on CI-like environment (like Jenkins, Travis, Gitlab CI, CircleCI, etc)
you can apply the same interface, the only difference is you'll need to get the URL for the remote driver instead of a path for a driver on your machine.

```java
import java.net.MalformedURLException;
import java.net.URL;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.remote.DesiredCapabilities;
import org.openqa.selenium.remote.RemoteWebDriver;

public class LocalRemoteDriver implements Driver {

    private final String url;

    public LocalRemoteDriver(final String url) {
        this.url = url;
    }

    @Override
    public WebDriver instance() {
        final DesiredCapabilities capability = DesiredCapabilities.firefox();
        try {
            return new RemoteWebDriver(new URL(this.url + "/wd/hub"), capability);
        } catch (final MalformedURLException ex) {
            throw new RuntimeException(ex.getMessage());
        }
    }
}
```

