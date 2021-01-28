---
layout: post
title: "A case for fourth-dimensional pockets"
meta_description: "A case for fourth-dimensional pockets"
date: 2019-12-06
categories: [testing, personal experience]
image: /assets/images/2019/08/doraemon.jpg
image_alt: a still from Doraemon 2005 animated series
caption: "Doraemon 2005 series"
---

I'm part of the generation of kids that grew up in Portugal watching Doraemon on TV. But not the latest generations, oh no no no, I am part of the "original" first batch actually, where many of us had their first lifetime experience learning how to read subtitles while watching something, since the audio was in Spanish. For many of us the original "version" of this Japanese cartoon will forever be Doraemon and all his friends speaking in Spanish, with the Portuguese translation underneath. If I speak acceptable Spanish today, I owe it in part to Doraemon series.

Doraemon left a mark in many of us because every episode was this incredible experience: Nobita or some other kid got into some trouble, and Doraemon just went ahead and took some technological device from his futuristic "4th dimensional" pocket - that would either "solve" the kid's problem, or cause even more problems. It was fascinating that this "robot Cat with no ears" from the future could have so many tricks up his sleeve, in this case inside his pocket. And it wasn't a magical pocket, no sir, it was technology from the future. That pocket could fit in any gadget without a problem.

By now you're probably wondering, why am I reading about some nostalgic post about some japanese "cartoon" (apologies, I meant manga/anime). I'll go straight to the point then:

> I can't help but feel that in the whole of the software industry, there's a number of colleagues of ours that have a belief that the human beings that make up software teams, in the limit, are made of the same material of the magical 4th dimensional pocket Doraemon had, and function like boxes that can all be molded into looking and acting in the same fashion and can literally churn out from within them the same marvelous gadgets, all in a reproducible fashion, just like every Doraemon could (yes, lore alert, Doraemon was not unique, he was in fact mass-produced in the future... ).

For some of our colleagues in the industry, imprinted in their hearts and their minds, each software team is made up of "units" of people, resources, and you can apply to these units the same system of rules, tools, libraries, ways of working, ways of interacting, ways of communicating, ways of approaching problems, and you'll still have yourself a cluster of teams who in theory will all work in the same way, produce the same spectacular results who all can be quickly replaced and interchanged, and who can also increase and decrease in size according to "load", just like any typical service deployed on a Kubernetes cluster made up of a few pods.

Someone defines the rule set about something in particular, or a set of standards, and each of the team members in each of their separate teams are "encouraged" (if they're submissive in personality, they're "kindly threatned") to follow the same rule set.

I understand and I'm compassionate towards our colleagues in the industry that have these beliefs. I respect them. But I can't help but feel oftentimes the "will" to have "one rule set to rule them all" is not taking into account a lot of important points with regards to the context of where these rules are trying to be enforced.

## The purpose of each team within the same project cluster can be different

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


## The falacy of potential gains/losses

The counter arguments against "uniquely handicapping" teams by enforcing uniform rule sets are usually fair arguments:
- Maybe the teams which the rule set is not working are savage "rebel teams", because nobody else is having problems with this rule set;
- In the event the entire "rebel" team is hit by a bus, surely no one will know how to carry on the torch;
- Interactions seem to be hard, since we don't interact in the same way;
- No one will be able to support the "rebel" team, because no one shares the same understanding of the "rebel team";
- ...

These are all, I think, valid counter arguments, but, if a team understands that to be effective towards the population of paleontologists they're serving, they need to use a specific tool, would it be right for me to stop that for the sake of having "uniformity" across teams? What would I gain/lose in practice?

- A "rebel team" isn't necessarily a team that has problems with a rule set - to the contraty, it might just be the case that it's the first team that works in such a way they naturally indentify the underliying limitations of the rule set;
- A "rebel team" isn't necessarily a dirty or savage team, that if hit by a bus, all their work is closed. To the contrary, Rebels understand that "passing the torch" is important to, if not for anything else, to propagate their rebel ideals (which is the mindset moving a lot of highly maintainable opensource projects for example);
- Some of the most meaningful interactions you might have are with people who are rebels in their own way, that don't abide by the norms of society, be it a genuine Christ-follower or a seasoned Communist, and the same applies in a software project. It goes without saying: a rebel isn't necessarily a rude or disrespecting person;
- Rebel teams don't need support - they are the kind of team that makes breakthroughs without waiting for someone else to make a brakethrough first and become accountable for their success/failure.
- ...

## The most important factor - is unique in itself

Humans are not pods. Humans are not soul-less machines. They can't be spinned up/down for load balancing. When you provide people the clear options, be on guard, because you'll quickly identify who views their team-members as "pods" and who views them as humans, depending on workloads and release "promises".

Each team, no matter if sharing the same underlying tools, libraries, code-based - is composed of different unique people. Each person is providing different tempos to the whole picture of their team and their project. How many of us know of cases where oftentimes it's just a single team member in the right place making a ton of difference (extremely positive, or extremely negative), no matter how many people we throw into the same team?

Time and time again, in my personal experience, I've seen cases of singular people or a small group of people working to exhaustment to not let their fellow colleagues down, more than to work for success of the project. Time and time again I've also see singular people who are toxic in their own way, and cause a negative impact on the team.

So threating the most important factor, the human element, as a number, is a complete folly. When you only see numbers you don't see context. You don't see underlying conections and dynamics.

No amount of team building can make up for the fact you built a toxic team. And in opposition, no amount of crappy challenges or crappy context can break bonds of a team that is organically "builded", that gives a sh%t about things, and ends up united by common threads that no team building exercise can create.

Ignoring the human factor is setting yourself up for default defeat.

## Release cycles and expectations are different, even withing the same "universe"

A release cycle of a team is not necessarily similar to the team next to it. "Duh!", right?

Do I have a problem with people following their own track? Nope. In fact, this is usually my approach when I have to guide and lead testers in different teams: *"Whatever works best for your context, you are empowered to do anything provided it will still accomplish your main mission as a tester - hunt down and signal the most important and meaningful bugs and risks about the product you're helping build, all in the time you're given".*

Let's pick back the example of the *FictionalPaleoApp*:
- A set day to deploy some chunk of code might make sense for a feature team that follows a tightly structured agenda, but it might hinder the efforts of a more hardcore (and possibly remote) team that needs deployments to happen asynchrounously;
- Some changes to specific teams require a lot of testing efforts to happen from design to deployment, while for other teams, a certain level of sanity checks can do the trick;
- A deployment freeze might make sense for the feature team that that does not deploy as often, but, it might not make sense for a team that is everyday deploying meaningful changes to production several times each day;

There's more cases similar to the above, but these portray already a need for release cycles to be adapted to the team's context. And this is even without starting to consider different stakeholders tradeoffs. Gerald Weinberg dedicated a whole chapter on his [Perfect Software](https://www.amazon.com/dp/B004J4VVE2/) book just about this: what a release means to different parties, and how it impacts each, generating entire dinamics between them. A common team goal is seldom a common individual goal when you're a tester, a developer, etc.

So it goes without saying: why would you try to clone release cycles between teams by force, without understanding that each teams's context oftentimes demands a unique and adapted release cycle?

## Not everyone's contribution is a contribution

Valuable contributions are not necessarily "voicing ones concerns while disregarding completely the most important element": the human element.

For example: Everyone can have an opinion on something, but, until they "do something", the act of having an opinion, or seemingly "appearing to be doing something" is not necessarily a contribution to the software project they're in.

In my personal experience I've seen people who churned out tons of code, some made a null lasting impact on the projects at hand, and some helped establish the projects they were in a success. I've seen people who had the title of "manager" in a team and closed themselves up in politics the whole of their work days, and people who didn't have a title but you'd follow them until the end. Not all humans, with the same title, with the same job description, with the same "curriculum" make meaningful and valuable contributions to a project - simply put - no single human is the same. We might be similar, we might have the same identifiers, but one is a lazy bastard and the other is a work horse.

So if you still consider your fellow humans as resources you can add or take from a software project - consider also that those resources don't produce the same, even if the packaging is the same. And allied with the previous factors described above - it's not mathematic: a mix of non contributors with contributors, is not necessarily increasing your chances of success of a software project.

## Wrapping up

A lot more can be said, but maybe in another post. Thank you for reading. Feel free to reach out to me with comments, ideas, grammar errors and suggestions via any of my social media, or by email, which you can find in my Github account. Until next time, take care!