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

Often when testing I don't have all the information, or all the facts. I'm most often hunting for them, based on observations and assumptions, using testing as a vehicle to find information about known unknowns, risks, and even dispell illusions I or any other member of my team has.

But there's trouble in this: by being based on my assumptions I'm not setting a "perfect" course nor am I going about with silver bullet material to start with. I end up directing my testing efforts oftentimes unknowingly (or distractedly) setting myself up to stumble upon unforseen troubles, unknown unknowns, or even apparent issues that become apparent, say, in the production deployement of what it is I am testing at any moment for example.

## Examples of stumbling

### 1) The apparent hidden characteristic

A lot of times specifications or acceptance criteria, or whatever it is you want to call it that seemingly helps you give boudaries to a problem, miss out on implicit criteria and implicit ideas that are held by different "actors". Even if one is not a very creative person, almost all planned (and unplanned) chunks of work leave some room for interpretation and implicit understandings, which then lead to stumbling of apparent things which looked hidden.

Confusing?

Say we're looking at a problem through a set mind, looking at what's apparent. The problem is something as trivial as finding the number of squares in a figure like the one bellow:


//TODO figure.


One might be tempted to count only the smallest of squares. One might be tempted to count the squares that are made up of smallest of squares as well. Some other person will also count the squares that are made up of the squares that are made up of smaller ones, and so on. And each of these people might believe to the core of their being they are looking at the problem correctly, which ultimately doesn't matter - if the criteria for solving the above problem leaves out this information, leaving room for interpretation and wrongful approaches towars solving the problem.

This is no different in the software development world, no matter how much specification we put into a chunk of work that some programmer is expected to finish a given amount of time.

This particular "Jump-to-meaning" ultimately leads to all involved (including Testers) to forget to look at the problem with more than one perspective, which later on cause problems that would be otherwise apparent problems.

### 2) The unforseen function

Following the clearest and "most important" user paths, forgetting that in the same context, any minimal user path could be an entryway for malicious usage, and is as important as the "largest-user-behaviour-fitting" paths, hence missed it during initial testing. /TODO

### 3) The unforseen load

Based my efforts on small event loads. Prepared for a number of times that small load, thinking it would shed some light on a bigger event. Ended up with dealing with a giant event - thinking that linerarity is still the case - problems follow. /TODO

### 4) The rush and "unforseen" disaster

Nowadays the software industry is plagued with a set of very nasty problems:

- That "Agile" can be about anything, specially about being "FAST" (when it is convenient), as oposed to, originally, a set of principles and ideas defined in a manifesto for the ("low-level") tasks of software development (aka. coding);
- The need to quantify things which are not really fully quantifiable in numbers, for example, Quality (here defined as a value relationship of something with someone);
- That "Agile Scrum Delivery Product Owner Managers Inc.", while being paid for the most part for the single responsibility to decide release timelines based on the information they should hold at any time of "what are the risks", "what seems to be ready", "what might we be missing", etc., relay that single responsiblity to Testers or to "QAs";
- Complete perversion the role of a Tester, which is to hunt down for the information mentioned before, and not to act as a magical "gatekeeper of bugs";
- Complete perversion of the role of someone responsible for quality assurance, which is, for the most part, to define multiple "keep everyone accountable/in check" processes, and not to act as a magical "assurer of quality";

All of these nasty problems often translate into sometimes we as Testers getting distracted: we're eager to accept the results of automated checks (which are not a replacement for meaningful testing), we trust the results, code gets merged, only for us to minutes/hours later realised: it would have been a better idea to run some experiments and test properly some parts that the automated checks will never complain about. And we find ourselves in situations where we missed very apparent bugs had we taken a mindful perspective instead.

The same applies when Testers share abstract (and not very meaningful) results with folks in delivery/management positions, for example, about number of test cases passed, or number of portions of work that have been tested. The delivery folks are often in a rush, uphold any of these non meaningful numbers as a global truth and the Testers fail to pass the most crucial message:
> "Guys, these numbers don't mean anything, in fact, we've been thinking, and these test cases only scratch the overall surface of what we have to test, we would like to test more deeply these specific experiment cases..."

I've seen this happening time and time again: based on people's observations, beliefs are built that something is ready, because the Testers have been "seemingly" testing for quite a while, when in reality the build they need to test or the environment is not ready. The truth is that a big time interval could have been spent doing other stuff while waiting for a build, or retesting and stumbling on issues which don't allow one to cover more of the whole system they need to test.


### 5) "The same model of the same car is the same everywhere"

This is probably the most prevalent example of stumbling usually held by either junior testers, or by all kinds of senior management and "delivery folks" who have a very narrow understanding of testing: the strong belief that whatever it is you test in a test/staging environment can be a strong "linear and confident" estimate of what you'll see in production. This is never the case for a simple reason: They're different systems.

Even with all the containerization and "infrastructure as code" one can set up, or no matter if they might follow the same structure and replication rule set to the most tiny detail: overall we're talking about different deployment environments, different 3rd party services connected, different persistence instances with different data (even if with the same version), different configuration, and different unexpected usage, among many other things which make the systems "the same", but at the same time, "different".

The worst mistake one might make is assuming that the systems are the same, or expecting them to be the same. That is not to say from now on we can be savages, and rule-less. No. We should aim and fight with teeth and nails for the systems to be similar and easily replicated anywhere as much as we can, and there's no excuse in 2019, with all the tools and libraries available to not try this. But, any thoughtful and alert team member never forgets, that we're always talking about unique instances of the same system. Nasty bugs often go unnoticed when we forget about this key detail, and when we trust logic to apply perfectly while forgetting that we ourselves are flawed, imperfect, and we build imperfect systems always.

## Meaning

/quote Gerald Weinberg book "perfect software" / "secrets of consulting" /TODO

## The problem of skipping towards meaning

/quote Gerald Weinberg book "perfect software" / "secrets of consulting" /TODO


## Controlling the tempo

/quote john boyd /TODO
/quote tempo book /TODO


## Wrapping up

/TODO