---
layout: post
title: "My Top 3 Favorite Test Engineering Anti-patterns"
description: "A look at usual mistakes/bad smells in Test Tooling & Engineering"
meta_description: "A look at usual mistakes/bad smells in Test Tooling & Engineering"
date: 2021-02-14
categories: [thought piece]
image: /assets/images/2021/02/jp_malcolm.jpg
image_alt: a movie still from Jurassic Park 1993
caption: "Jurassic Park, 1993"
---

After working in Software Testing and Test Tooling long enough, one notices repeating "responses" to certain Testing/Quality related problems that are fruitless and inadequate. In this post I will try to go over some of which me and many friends in the craft have observed through the years.

## *"The Wheel Reinvention Loop"* anti-pattern

This is one of the most common for Testers and Test Engineers (read, Coding Testers). It usually starts with this "*what*":

> *"old test engineer left the project, long live new test engineer"*

Depending on the context and culture of the project the above means almost always an act of "*reinventing the wheel*", in other words:

> *Let's scrap everything the old test engineer did, start anew, create brand new tooling and scripts and adapt a different framework (or even programming language) to start our automated checks from scrap, ...*

Most folks have done it and fallen victims to this scheme. Nobody is innocent, even I have fallen victim to the Siren song too. There's different flavours for this anti-pattern, or the "*how*":

- The previous Test Engineer leaves due to a myriad of reasons, which can be [Test or Human-related](https://filfreire.com/posts/quality_bandits). Reasons ultimately are **noise** in the productivity of both regular testing efforts and typical automation related development.

- The sources of **noise** are varied. They might be due to outside-of-the-project influence, which deprecate/sabotage the work of the Test Engineer: from people outside of the project imposing or demanding "standards and best practices" to the Test Engineer reaching tooling limitations or falling over other anti-patterns.

- The period of hiring a replacement contributes to the deprecation of the work done by the previous Test Engineers. If the project is unlucky, it will start patching its lack of people with absurdities like "we don't need neither dedicated Testers nor do we need Test Engineers" or [testing sweatshops](https://filfreire.com/posts/dystopian_future).


- Testing and Quality problems increase, become of monster magnitudes, and any new Tester/Test Engineer that is thrown into the problem inevitably starts impaired. These start-conditions can be so hardcore that they make-or-break most Testers/Test Engineers. Few stay in the craft if they are thrown into these recurrently without any support.

- A new Test Engineer appears! They join the project, finds themselves with a deprecated project and tools and moldy evidence of scripted testing, and decide to start everything anew, propelling themselves to a soon-to-be sunk-cost scenario: *we had to start everything from scratch, management/external forces demanded from us a certain level of production so we took some decisions that we now have to continue doing things the way we do*.

- **Noise** and sunk-cost come into play again and again, and it's only a matter of time until the cycle restarts.

<figure>
    <img src="/assets/images/2021/02/typical_cycle.jpg" alt="The Wheel Reinvention Loop anti-pattern" style="max-height: 550px;">
    <figcaption>A figure of the "The Wheel Reinvention Loop" anti-pattern</figcaption>
</figure>

We have covered (more or less) the **what** and the **how**. To cover the **why** let's first look at 2 other anti-patterns, we'll get back to it in the end of this post.

## *"Gherkin/Cucumber to ease/enable ..."* anti-pattern

> "*Here Here! A decision has to be made! We will represent our test cases/automated checks in a human readable-language so that XYZ can interact with them!*"

This anti-pattern is probably one of the most publicly debated ones, as it's also a famous point of clash between schools of testing. When a strong emphasis is given on the portrayal of scripted testing scenarios there are two roads.

The *road most traveled* is the one of (attempting) to portray said scripted testing scenarios within the confines of `Given-When-Then-*` or similar language constructs offered by Cucumber/Gherkin. It is a road that leads to affliction/damnation.

The *road less traveled* (and the one that leads to good fortune) is the one where folks don't waste precious time representing tests in a human readable fashion and instead learned a few immutable truths:

- Product/management people will never (read "*99.99999% of the times*") write, read, maintain, appreciate, study, constructively-criticize or make use of any scenarios, be them written within the confines of Cucumber or scribbled in graffiti next to the copy of Mona Lisa sitting on the Louvre;

- The self-imposed structure of `Given-When-Then-*` is limiting for any actually relevant scripted testing scenarios. You code enough scenarios in your lifetime you will reach the same conclusion. Why? First, most software we write is like a joke at deterministic systems, and second, *life cannot be contained*: *Jurassic Park*'s brightest engineers loved `Given-When-Then-*`, now they're jobless (or dead);

- Using human readable language as a representation of tests is naive/senseless if humans themselves can't agree on what to write/read when it comes to behavior of a product leading to all kinds of time wasting discussions (e.g. *"Should this step of the scenario validate this one web element, or one step represents a complete user flow???"*);

- ...

For the 0.000001% of the test engineering population that can still make effective and appropriate use of structured human dialects to represent scripted testing scenarios, sure, it's not an anti-pattern, but for everyone else, writing a `.feature` file is as fruitful as tears in the rain, it is work that is done to show that work is being done, but that is doomed to be deprecated as a portrait of a given test script the moment it is written.

The solution for this anti-pattern: **don't waste time with embellishing the portrait of scenarios if you have to encode them, use that time to make the scenarios more meaningful**.

**Practical example**: there's a million ways to write a Gherkin scenario for a login page, in the meantime, a 15 year-old kid has all your production keys and secrets, and a 13 year-old kid got all your stock of Action-Man figures shipped to a warehouse to re-ship and resell it to New Zealand. You could have caught both the kids by doing the simple Python script that they did... You sure you want to waste time and money on that `.feature` file? Which pursuit is more meaningful in your context?

## *"The Cult of Dashboards and Links"* anti-pattern

I've written [in other words](https://filfreire.com/posts/quality_infotainment) about this anti-pattern already.

It's an easy one to identify, but a hard one to fix. If you notice this in your project:

- There's a disproportion between the emphasis of linking and tracing (tons of) scenarios on Ticketing Systems versus the **usefulness** of said scenarios.
- There's a disparity between scripted test execution results (be them done by actual people or automated checks) and how **actionable** those results are.

*Ye' be warned*. These are cues for the software development equivalent of a "*self-harm cult/sect*". If you want to know more about it, I got into some detail in the [other post](https://filfreire.com/posts/quality_infotainment).

How to fix this anti-pattern? A good start at it is to become very hardcore about **usefulness and quality** ***over*** **display and quantity**. It's better to have a smaller subset of scripted tests / automated checks and when they fail they are either flagging something serious to your project or they help convey symptoms that your project is in an unhealthy state... than to keep track of pass/fail ratios, percentages and bug counts to later [show to senior management as a scam](https://filfreire.com/posts/quality_bandits).

**Practical Example**: if development and staging environments are constantly unhealthy and untestable, don't hide it in your automated checks. And more important than complaining about those environments failing, is making sure the failure notices are actionable by the team. In other words, it is one thing to say

> something is not working, [please check my failed jenkins job](https://filfreire.com/posts/lost_art) and the ticket 1234 of the test case on JIRA

versus saying

> *SomeAutoChatbot says*: The endpoint ABC in development environment 029 is failing with 502 Bad Gateway for the `buy-an-action-man` test scenario. Error trace-id is `053de188-7438-42b1`. Link to the logs `some kibana/cloudwatch link`. Possible solution: restart the orders service `here` or contact @oncall-support-dev-env-team.

A moment for reflection: How many of us keep *throwing sand into the air* and opting for the former and not the latter? What is stopping us from pursuing the *road less travelled*?

## How do we beat the *reinventing wheel loop* anti-pattern?

Getting back to the "*why*" of the first mentioned anti-pattern and, in a way, all these other ones.

These anti-patterns afflict and/or have afflicted every test engineer in the world at least once. The *why* is, based on my personal (and faulty) interpretation is simply put: a lack of initial well grounded insight and perspective on Testing and Test Engineering... (aka *"falta de noção"* 🇵🇹)

This lack of insight is, I believe, boosted by different variables:
- the fact that most of us get into Testing or Test Engineering without any literacy and meaningful knowledge on the same topics;
- many Testers (and non Testers) remain illiterate about Testing for their entire shelf-lives as Testers and then onwards as Coders or Managers and even Senior Managers;
- there are several "schools of thought" on Testing worried about illiteracy overall, but that are oftentimes too busy in battles with each other or trying to survive and remain in demand;
- context-driven schools of Testing practically only care about the Testing side of the illiteracy problem, and are unable to tackle modern-day Test Engineering needs;
- non-context-driven schools of Testing only care about the Automation in Test/Test Engineering/Tooling side of the problem are are oblivious to the "Testing as a craft" side;
- ...

And in the meantime, software projects everywhere keep bumping into the same potholes on the same spacious roads, until a few Testers or Test Engineers "get woke".

As some of you might have experienced: This definitely doesn't scale for most software projects' needs and people end up throwing more anti-patterns at the problem in hopes of quick-fixes.

**There is hope.** The best approaches I learned so far to solve these anti-patterns are:

- On Test Engineering & Tooling side: a strong focus on making any tooling nimble and useful, discarding the rest as *smoke-selling*.
- And on Testing side of the scale: a herculean focus on making Testing deep, experiential and meaningful.

These two sides need to help each other for the magic to happen. There are a few practical ways to achieve this, but I'll leave those for another post and time. If you want to know more, stay tunned :-)

________

_If you read this far, thank you. Feel free to reach out to me with comments, ideas, grammar errors, and suggestions via any of my social media. Until next time, stay safe, take care! If you are up for it, you can also <a href="https://www.buymeacoffee.com/filipefreire">buy me a coffee ☕</a>_
