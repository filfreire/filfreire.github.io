---
layout: post
title: "The lost art of checking failed CI jobs"
meta_description: "The lost art of checking failed CI jobs"
date: 2020-09-28
categories: [testing, personal experience]
image: /assets/images/2019/05/deltaforce.jpg
caption: "Delta Force, 1986"
---


If you've spend some time doing work around Software Engineering in modern web or app development environments, with moderate-to-big team sizes, you've by now found on occasions the following interaction at least once between 2 (or more persons),

```
Person A: Hello

* waits for Person B to reply

Person B: Hey what's up?
(Person B frowns at the screen, as a Foreshadowing of what's about to happen)

Person A: My jenkins job is failing. Can you check?

(Person B's brain is parsing 'check' as 'fix it for me cuz i'm dumb'... heart rate and feelings of anger intensify)

Person B: Ok... can you be more specific?

(Person B frowns at the screen, as a Foreshadowing of what's about to happen)

Person A: the job to build XYZ. please check quickly, I am blocked by this!!!!!!!

Person B: Ok... can you give me a link?

Person A: its on jenkins... but ok, give me 1 minute

(25 minutes pass by)

Person A: here is the link: <provides the link to the jenkins job but not to their affected build log>
please do something about it, our team is blocked by this!!!!!!!
```

There's a good chance you've seen also different flavours of the above dialogue, usually almost always conducted between someone who has a problem but for one reason or the other cannot solve it or describe it in detail, and another person, whose time is "stolen" to do a big chunk of something that the first person could have done to get closer to a solution of the problem. Usual suspects are:

- The tester that says, enigmatically "something is failing", and leaves to eat a donut;
- The developer who "doesn't know" on knowing how to use a simple tool to perform a task and then asks another developer to do the task instead;
- The manager/product owner/agile-something that asks the status of a ticket without the intention actually knowing the status (and usually the ask itself serves no purpose other than a psychosomatic outburst);
- The staff engineer or tech lead that has no foundations towards basic development tooling, and will ask recurrently the same questions to interns and juniors;
- ...


More often than not, besides the clear faulty communication flow, and sometimes the handicaps in either knowledge, willpower or trust of one of the parties involved in the problem discussion, have different meta-problem levels surrounding the original technical problem. 

In this post I'd like to go a bit into these meta-problem levels.


## Lack of trust

/TODO
"you don't trust others enough to value their time"
"you don't trust yourself"

## Lack of willpower (aka Laziness)

/TODO

## Missing Foundations

/TODO

## Clogged communication pipelines

/TODO

## Lack of documentation

/TODO

## Lack of habit

/TODO

## Wrapping up

/TODO
