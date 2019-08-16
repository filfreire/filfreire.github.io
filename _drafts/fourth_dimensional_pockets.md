---
layout: post
title: "A case for fourth-dimensional pockets (draft)"
meta_description: "A case for fourth-dimensional pockets (draft)"
date: 2019-08-16
categories: [testing, personal experience]
image: /assets/images/2019/08/doraemon.jpg
caption: "Doraemon 2005 series"
---

I'm part of the generation of kids that grew up in Portugal watching Doraemon on TV. But not the latest generations, oh no no no, I am part of the "original" first batch actually, where many of us had their first lifetime experience learning how to read subtitles while watching something, since the audio was in Spanish. For many of us the original "version" of this Japanese cartoon will forever be Doraemon and all his friends speaking in Spanish, with the Portuguese translation underneath. If I speak decent-acceptable Spanish today, I owe it in part to Doraemon series.

Doraemon left a mark in many of us because every episode was this incredible experience: Nobita or some other kid got into some trouble, and Doraemon just went ahead and took some technological device from his futuristic "4th dimensional" pocket - that would either "solve" the kid's problem, or cause even more problems. It was fascinating that this "robot cat with no ears" from the future could have so many tricks up his sleeve, in this case inside his pocket. And it wasn't a magical pocket, no sir, it was technology from the future. That pocket could fit in any gadget without a problem.

By now you're probably wondering, why am I reading about some nostalgic post about some japanese "cartoon" (apologies, I meant manga/anime). I'll go straight to the point then:

> I can't help but feel that in the whole of the software industry, there's a number of colleagues of ours that have a belief that software teams, in the limit, are some sort of magical 4th dimensional pockets or boxes that can all be molded into looking and acting in the same fashion and can literally churn out from within them the same marvelous gadgets, all in a reproducible fashion, just like every Doraemon  could(yes, lore alert, Doraemon was not unique, he was in fact mass-produced in the future... ).

For some of our colleagues in the industry, imprinted in their hearts and their minds, each software team is made up of "units" of people, and you can apply to these units the same system of rules, tools, libraries, ways of working, ways of interacting, ways of communicating, ways of approaching problems, and you'll still have yourself a cluster of teams who in theory will all work in the same way, produce the same spectacular results who all can be quickly replaced and interchanged, and who can also increase and decrease in size according to "load", just like any typical service deployed on a Kubernetes cluster made up of a few pods.

Someone defines the rule set about something in particular, and each of the team members in each of their separate teams are "encouraged" (if they're submissive in personality, they're "kindly threatened") to follow the same rule set.

I understand and I'm compassionate towards our colleagues in the industry that have these beliefs. I respect them. But I can't help but feel oftentimes the "will" to have "one rule set to rule them all" is not taking into account a lot of important points with regards to the context of where these rules are trying to be enforced.

## The purpose of each team within the same cluster can be different

Context matters and it's different across any team, no matter if the team is part of the same cluster of teams and working for the same "purpose/product", dedicated to a small part of it.

Let's say I'm working in a mobile app for Paleontologists, called *FictionalPaleoApp* (trademark pending). The app has grown and is now used both by students as well as famous palentologists that work as tour guides on the new Jurassic Park that will open in Portugal in 2035.

My team setup would look a bit like this:
- I have one team who works on the part where a user can see the latest fossil findings across the globe;
- Another team will work on a dedicated spaces part of the app so there will be specific spaces for people who only study plants from the Triassic and Jurassic period, or another space for people who only study behavior of Raptor class of Dinossaurs;
- And then there would be other teams for other imaginary parts of the app...

Even though all of the teams are working for the same final product, each of the teams is for the most part foccused on delivering different experiences and interactions within the same application.

So what's stopping me of making all the teams working in the same way, you might ask? Nothing. Each team is empowered to work in the same way, and approach problems in the same fashion.

Except for the fact that they're working in different scopes and in producing different "deliverables", it shouldn't make a lot of difference, right? I don't think so. It's a folly to look at software teams as a set of uniform-looking groups when each of their end goals is different, no matter if they all work on the same codebases, with same tools, in the same deployment space.

To use the same fictional scenario: The team that is dedicated on displaying gigabyte sized images of fossils in the same app, has different underlying motivations than the team foccused on the feed for "latest trends in fossils".

From my personal experience: different motivations and different problems by default require adapted ways of approach, and it just might be the case they require completely different approaches.

One of my team mates might say, we're all *FictionalPaleoApp*, we all do things in the same way here... But then if my goal is uniformity in the rule set I apply/enforce to all teams, I must live with the consequence that I might be setting myself up to have teams in which my rule set makes them uniquely handicapped by design.


## The falacy of gains

The counter arguments against "uniquely handicapping" teams by enforcing uniform rule sets are usually fair arguments:
- Maybe the teams which the rule set is not working are savage "rebel teams", because nobody else is having problems with this rule set;
- In the event the entire "rebel" team is hit by a bus, surely no one will know how to carry on the torch;
- Interactions seem to be hard, since we don't interact in the same way;
- No one will be able to support the "rebel" team, because no one shares the same understanding of the "rebel team";
- ...

These are all, I think, valid counter arguments.

But, if a team understands that to be effective towards the population of paleontologists they're serving, they need to use a specific tool, would it be right for me to stop that for the sake of having "uniformity" across teams? What would I gain/lose in practice?

/TODO

## The most important factor - is unique in itself

Humans are not pods and can't be spinned up/down for load balancing. When you provide people the clear options, be on guard, because you'll quickly identify who views their team-members as "pods" and who views them as humans, depending on workloads and release "promises".

Each team, no matter if sharing the same underlying tools, libraries, code-based - is composed of different unique people. Each person is providing different tempos to the whole picture of their team and their project. How many of us know of cases where oftentimes it's just a single team member in the right place making a ton of difference (extremely positive, or extremely negative), no matter how many people we throw into the same team?

/TODO

## Release cycles and expectations are different, even withing the same "universe"

A release cycle of a team is not necessarily similar to the team next to it.

Do I have a problem with people following their own track? Nope. "Whatever works best for their context, they are empowered to do anything provided it will still accomplish their main mission as a tester - hunt down and signal the most important and meaningful bugs and risks about the product in the time they're given".

/TODO

## Not everyone's contribution is a contribution

Valuable contributions are not necessarily "voicing ones concerns while disregarding completely the most important element": the human element.

/TODO

## Expectations are not "unitary"

Expectations can be similar explicitely, but never implicitly - within the team, within ˝stakeholders", within actual stakeholders, etc.

/TODO


## Wrapping up

/TODO