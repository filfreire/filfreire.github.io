---
layout: post
title: "Jumping to meanings"
meta_description: "Jumping to meanings"
date: 2019-05-22
categories: [testing, personal experience]
image: /assets/images/2019/07/shooter.jpg
caption: "Shooter, 2007"
---

A lot of times when doing hands-on experiencial testing, or preparing data for a load test, or even reviewing and coding unit checks I find myself jumping to conclusions.

The explanation of the psycological term witht the same name goes about somethig like this:

> "communication obstacle where one "judge[s] or decide[s] something without having all the facts; to reach unwarranted conclusions" ([link](https://en.wikipedia.org/wiki/Jumping_to_conclusions))

The thing, often when testing I don't have all the information, or all the facts. I'm most often hunting for them, based on observations and assumptions, using testing as a vehicle to find information about known unknowns, risks, and even dispell illusions I or any other member of my team has.

But there's trouble in this: by being based on my assumptions I'm not setting a "perfect" course nor going about with silver bullet material to start with. I end up directing my testing efforts oftetimes unknowingly (or distractedly) setting myself up to stumble upon unforseen troubles, unknown unknowns, or apparent issues that are apparent, say, in the production deployement of what it is I am testing at any moment for example.

## Examples of stumbling

### 1) The apparent hidden characteristic

Looking at a problem through a set mind, looking at what's apparent, and forgetting to look at the problem with more than one perspective. /TODO - (example "finding all squares in a figure")

### 2) The unforseen function

Following the clearest and "most important" user paths, forgetting that in the same context, any minimal user path could be an entryway for malicious usage, and is as important as the "largest-user-behaviour-fitting" paths, hence missed it during initial testing. /TODO

### 3) The unforseen load

Based my efforts on small event loads. Prepared for a number of times that small load, thinking it would shed some light on a bigger event. Ended up with dealing with a giant event - thinking that linerarity is still the case - problems follow. /TODO

### 4) The rush and later disaster

Sometimes we get distracted, we're eager to accept the results of automated checks (which are not a replacement for meaningful testing), we trust the results, code gets merged, only for us to minutes/hours later realised: it would have been a better idea to run some experiments and test properly some parts that the automated checks will never complain about. And we find ourselves in situations where we missed very apparent bugs had we taken a mindful perspective instead.

### 5) The unseen blockades

I've seen this happening time and time again: based on people's observations, beliefs are built that something is ready, because the Testers have been seemingly testing for quite a while, and the truth is that a lot of that time interval could have been spent doing other stuff while waiting for a build, or retesting and stumbling on issues.

## Meaning

/quote Gerald Weinberg book "perfect software" / "secrets of consulting" /TODO

## The problem of skipping towards meaning

/quote Gerald Weinberg book "perfect software" / "secrets of consulting" /TODO


## Controlling the tempo

/quote john boyd /TODO
/quote tempo book /TODO


## Wrapping up

/TODO