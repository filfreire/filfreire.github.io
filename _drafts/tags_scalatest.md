---
layout: post
title: "Grouping tests in scala made easy"
date: 2018-05-17
categories: [scala, grouping, tags, testing, scalatest]
---

tagging a scenario:
```
class ProductCartTest extends FlatSpec with Eventually with CustomPatience {

//...

it should "update total price on item removal with success" taggedAs (SlowTest) in {
```

You also need an object to create a tag:
```
import org.scalatest.Tag

object SlowTest extends Tag("com.your.package.SlowTest")
```

And then you can customize your maven profile to include or exclude tests with given tags, example for `tagsToInclude`:
```
<profile>
    <id>integration-tests</id>
    <build>
        <plugins>
            <plugin>
                <groupId>org.scalatest</groupId>
                <artifactId>scalatest-maven-plugin</artifactId>
                <configuration>
                    <parallel>false</parallel>
                    <tagsToInclude>com.your.package.SlowTest</tagsToInclude>
                </configuration>
            </plugin>
<!-- ... -->
```

Documentation worth checking out:

- One instance of fixture per test: http://doc.scalatest.org/1.8/org/scalatest/OneInstancePerTest.html
- More info on FlatSpec: http://doc.scalatest.org/1.8/org/scalatest/FlatSpec.html
- Scalatest maven plugin: http://www.scalatest.org/user\_guide/using\_the\_scalatest\_maven\_plugin
- Suite: http://doc.scalatest.org/1.8/org/scalatest/Suite.html
- FlatSpec: http://doc.scalatest.org/1.8/org/scalatest/FlatSpec.html

To investigate: https://www.scalacheck.org/
