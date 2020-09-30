---
layout: post
title: "The lost art of checking failed CI jobs"
meta_description: "The lost art of checking failed CI jobs"
date: 2020-09-28
categories: [testing, personal experience]
image: /assets/images/2019/05/deltaforce.jpg
caption: "Delta Force, 1986"
---


Have you ever found yourself in either end of the following interaction between 2 or more persons:

## _"Can you fix my Jenkins job?"_

```
Person A: Hello

* waits for Person B to reply

Person B: Hey what's up?
(Person B frowns at the screen, as a Foreshadowing of what's about to happen)

Person A: My Jenkins job is failing. Can you check?

(Person B's brain is parsing 'check' as 'fix it for me'... heart rate and feelings of anger intensify)

Person B: Ok... can you be more specific?

(Person B frowns at the screen, as a Foreshadowing of what's about to happen)

Person A: the job to build XYZ. please check quickly, I am blocked by this!!!!!!!

Person B: Ok... can you give me a link?

Person A: it's on Jenkins... but ok, give me 1 minute

(25 minutes pass by)

Person A: here is the link: <provides the link to the Jenkins job but not to their affected build log>
please do something about it, our team is blocked by this!!!!!!!
```

## _"Can you fix my problem(s)?"_

There's a good chance you've seen and took part also on different flavours of the above dialogue. And the kicker most times is the dialogue is not guaranteed to be on something that is indeed to be deemed "mission critical".

These dialogues are done between someone who poses a problem, but poses it barely, with little detail, insight or previous "homework", and another person, who will act as a "problem-solver" (and indirectly as the effective "problem-poser"). This latter is more often than not already pursuing a task, and their time ends up being diverted to a great extent, being left with feelings that the former person could have at least eased up the task to get closer to a solution of the problem.

Some of the most common day-to-day flavours are:

- The tester that says, enigmatically "something is failing", and right away leaves the dialogue in a cliffhanger and goes do something else;
- The developer who "doesn't know" on knowing how to use a simple tool to perform a task and then asks another developer to do the task instead;
- The manager/product owner/agile-something that asks the status of a ticket without the intention actually knowing the status (and usually the ask itself serves no purpose other than a psychosomatic outburst);
- The staff engineer or tech lead that has no foundations towards basic development tooling, and will ask recurrently the same questions to interns and juniors;
- ...

Besides the clear faulty (or weird) communication flow, and perhaps lapses/faults in knowledge, willpower or trust of one of the parties involved in the problem discussion, the problem is actually a face of a much bigger metaproblem that emcompasses the inintial problems.

I'd like to go over what I think the different faces of the bigger metaproblem might be, in no particular order:

## Lack of documentation

The most naive of us, or read, those of us who haven't been bruised by a few "career-limiting moves" here and there, and the scars these problems sometimes leave, specially when mixed with tipical "tribal" intra and inter-team quarrels that happen a lot in the corporate world, will go forth and say:

> Surely the problem (and solution) lies in the lack of documentation!

Fair enough. We all know our "ABCs":
A - Documentation in tech projects is not easy;
B - Good documentation in tech projects is hard;
B - Good and meaningful documentation in tech projects is "[Call Of Duty Realism](https://callofduty.fandom.com/wiki/Realism)" dificulty;

Now, let's challenge this "lack of documentation" bit for a moment. It's hard to document if the architecture and process itself is confusing. If it's not __confusing__, it could be the case that, say, for a newcomer (or even a senior tech person) the documentation isn't easily __accessible__. So I can't necessarily blame someone for not being able to check by themselves build logs, or application logs, or how to go about building something on their machines, and many more actions, if for any of these tipical tech project actions the documents only show that the actions are confusing, or the documents are inaccessible, or even worse, the documents are supposedly clear and accessible, but not fully "translatable" without some other bits of implicit knowledge. Maybe an API token. Maybe a password. Maybe a URL that changed recently. Who knows right?

## Clogged communication pipelines

/TODO
talk abou the saying that comms are an image of the corporate structure and culture

## Lack of trust

/TODO
"you don't trust others enough to value their time"
"you don't trust yourself"

## Lack of willpower and habit

/TODO
what are the incentives
good intentions, mean spirits, Simple Sabotage Field Manual

## The inverted scenario

There's an extra "flavour" of the dialogue that I didn't mention up until now, that takes a mixture of all of the above meta problems
The "inverted scenario" of someone posing an actual serious problem, going to a certain length explaining it in detail, laying the common ground... and the other person acknowledges the problem by acting out the meme  "I must go now, my people need me!" or adding you to their "mental `.gitignore`".

This one is a catch-all scenario.

A somewhat sad reality will kick in through time: even if in a team, you and your friends make it part of your character values to invest in meaningful documentation, context-adapted effective foundations, unclogged communication pipelines, brotherly trust, and ultimate willpower and habit... there's somewhere inside (or outside) the organization a living antithesis to these values. Sort of an organisational ode to the "[darkest timelime](https://community-sitcom.fandom.com/wiki/Darkest_Timeline)" in the Community series.

Examples:
- The colleague(s) who is (or plays) lost on how to debug an issue, "is blocked" no matter how much useful debug info you provide;
- The manager(s) who is (or plays) unaware towards fixing ingrained cultural problems, that the tea
- The "other team"(s) that is clueless on how to solve a problem of theirs, even if you give them multitudes of evidence of what the problem is;
- Explaining in transparent detail (foundation-shattering) issues with suboptimal "corporate employee retention" practices (if they do exist), to be met with `old-man-shrug.jpg` meme by senior leadership or folks in charge of human _nuts and bolts_;
- ...

## Wrapping up

I personally don't have a good solution or follow-up to this last scenario. It's said _"it takes two to Tango"_ so one day we're the bad guys, some other day we're the good guys. The world is a messy and beautiful place. If anything, I think being aware of this metaproblem is a first-step at solving it, in whatever context we are on. Care to take a second step? Let's do it together, on 3:

One. Two.


_Thank you for reading. Feel free to reach out to me with comments, ideas, grammar errors, and suggestions via any of my social media. Until next time, take care!_