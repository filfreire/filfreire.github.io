---
layout: post
title: "(DRAFT) Rookie Python"
meta_description: "(DRAFT) Rookie Python"
date: 2019-07-04
categories: [draft]
image: /assets/images/jp_404.jpg
caption: "Replace this, 2019"
---

## setting up a proper local dev environment 

(avoiding weird "python is also installed elsewhere" states)
//TODO

## How do "build" my module and run the automated checks

What's the equivalent of "npm run test" or "yarn clean && yarn test" or "mvn clean test"? In some cases this will do the trick:

```
python3 setup.py test
python3 setup.py install
```

## how do i use a fork / altered local module instead of the one that comes from the internet

"I want to hack my own version of a module and then use it on my other project"

1. Clone the repo of the module you want to change (or your own fork).
2. Run test/install
3. Run `pip install --editable .`

(Source: https://stackoverflow.com/q/35064426)


## how do i publish a module to the world

//TODO
to the "npmjs.com"/ "rubygems.org" equivalent

//TODO checkout https://python-poetry.org/

## debugging?

how can i debug code using an approach like:

-- visual studio code + bash (macOSX & linux)
-- visual studio code + bash (windows subsystem for linux) ([vs code + wsl](https://code.visualstudio.com/docs/remote/wsl))

//TODO

(advice from valignatev -  some people prefer PyCharm, some people use vscode + lsp from mycrosoft, many people use TUI debuggers like pudb, and also lots of people use DAP on top of vim/emacs)

## how do i create a project from the ground up and publish it to the internet?

//TODO
