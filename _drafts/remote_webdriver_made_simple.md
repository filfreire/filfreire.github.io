# RemoteWebdriver made simple

## TL;DR:

If you need to quickly do some scraping of "static"-like pages you can setup a system to:
- raise a docker container with firefox+webdriver standalone
- have a maven project that produces an executable jar with your scraping
- run the jar given arguments (getting the webdriver host "dinamically", login data, scrape target data)
- kill the docker container
- extra: put it on a CI Job (example 1: jenkins; example 2: gitlab ci; example 3: travis)
