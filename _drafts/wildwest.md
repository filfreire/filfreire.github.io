---
layout: post
title: "A tale of the (Testers) Wild West"
date: 2019-02-03
categories: [rules, development, quality]
image: /assets/images/2019/02/rdr2.jpg
caption: "Red Dead Redemption 2, 2018"
---

Recently I came by this comment made by someone working in some unknown tech company:

> “(...) but the tech lead will not allow testers have a look at any code.”

I instantly felt triggered, offended, and whatever it is that people say to express how disgusted they feel with something that seems "unbelievable". For moments I thought I was being told a story of the wild west, of times when gunslingers and outlaws roamed and made the rules.

This is a "no brainer" for me: without having a lot of context, possibly after a couple of attempts to improve, I’d happily leave that company/project ASAP.

Firstly, and personally, because as a coder and opensource contributor, I find it's neglectful to ignore and ban others of the possibility of reviewing your code and your code changes. It's just stupid.

Secondly, and also personally, as a tester I don't take anything for granted, and I know through experience that programmers are bound to screw up. Some of them, though professional and mature (no matter the seniority level), because they make mistakes, as anyone does. In fact, everyone screws up, both testers, developers, managers, ...

For example, let's look a bit into this fictional scenario:

> **Coder**: _"Hey tester, you can test this, it is ready, deployed, done, I've finished the validation of all of these inputs"_
>
> **Tester**: _"It's not ready, squeal all you want, but finish your stuff first."_

Why? A simple 2-min read through the code showed me beforehand that developer only finished (and badly), the validation for the first input. And this scenario (and it's different mutations) is not that unusual and not that impossible, no matter how much validation and peer-review goes through the code before the testers get their hands on it.

Unless the code involves launching of nuclear missiles or some top secret confidential national security stuff (and even then…), I expect the same kind of access to it as a tester, as any contributor has to an open-source project: I want to see the code, the logs, the monitoring, the deployement information, the code quality and static analysis reports, the different environments, the discussions, I want to have the ability to investigate everything and anything that will influence my testing efforts.

Recently another colleague shared an article on a Slack group, a link with an interesting and thoughtful article of ["whether it's important or not for testers to have the power to read pull requests"](https://dustyjuhl.com/2019/01/14/is-it-important-for-testers-to-read-pull-requests/).

The article is spot on, and to me it's so much more than a matter of "importance" of reading PRs: I simply consider it a vital part of my job, and a crucial tool in studying code changes. As mentioned also in the above article, it's a shortcut to indentifiying some category of issues very early on the development process (earlier than that being "contesting" a development's specification even before a developer grabs it and starts working on it, like for example a ticket with no description and a crappy title). Again, it's a "no brainer".

Some argue that, no matter if the tester is also a developer, or has decent software engineering concepts, that there's more value in not necessarily the tester reading through the actual code of the PR, but more on tackling the PR in other ways:
- Read the commit messages (supposing they're made by non-sloppy programmers) to understand what's being brought in or removed;
- If the "continuous-integration" is mature enought in the project, go straight to testing the "pre-flight" deployement build of that branch even before the code gets merged to the main branch (and hence deployed to a staging/testing environment).

I subscribe both of these. As a tester I won't have time to do everything, and what matters the most to the project is how much of my time is spent doing actual valuable testing. I say: whatever works best for each, and to each project it's context applies. On the other hand, not having the possibility of choice, and being purposefully obscured/prohibited of seeing code changes when I need to know them and see them, under the guise of some architect's stupidity and lack of knowledge of healthy software development lifecycle: to me that's "blasphemy".


## But what of the testers that can't read code?

This is a falacy and also it's fake news. Unless you're an non-coder european/american reviewing code that was done with Chinese or Japanese characters, if you can read english, you can review code, you can review a pull-request and still extract valuable info from it. You might not know how to code, or the intricacies of the language, but you certainly know how to ask questions. So what's the problem?

If it's the problem of reading code: Almost all of the common workplace programming languages are "english", and interpretation of the code is not that difficultm, you get the "idea" of things, so you can ask a question when you spot something weird. And when you don't get the idea or get the wrong idea, again, you can ask. You don't need to be a computer scientist or some wizard mathematician in order to be able to read code.

Put into simpler words and based on my experience:

> Non-coders can participate in code reviews/pull-requests and still make constructive contributions to say, a given pull request by “more-or-less” understanding the purpose of the code change (they can read english), and asking seemingly “dumb” questions and looking for information (that in turn might even make programmers notice issues).

Some may say:

> But these testers asking me stuff is a nuissance!

So you're a junior developer then? Fresh out of ~~school~~ kindergarten? Do you want your mommy? I take it back, even this is an insult to some Junior Developers I know, who are very mature.

Ok, Yes, sure at times it's noisy. But the noise is also a valuable bit of info for me about the project. Talks to me a lot about inter-personal relationships in a project, for example. I subscribe that we need to build a good relationship with developers beforehand, because the nuissanse is there even for testers who are coders and fully understand the code... and some developers don't like to be asked questions by anyone at all. This won't change any time soon, and will happen in every single muliple-people project, guaranteed.

But not having the ability to ask anything at all: that's plain dumb. It is purposely not using a valuable brain with no context on your solution to mentally "pick on it" and see it in a perspective you haven't seen it as a developer.

You get the idea.

## A sin is never alone

I've come to learn that, the same way that in one's spiritual life a sin is never alone by itself (meaning we usually do more wrong than what we may recognize), the same applies for "sins" in software development process, and it's the same in this story:
As if it weren't enough, this matter of "secret-society and hidden from testers-code and pull requests" inside the workplace was not the only major "sin" promoted by this colleague's "architect/tech lead", the usual "sins" carried on:

- Release notes missing 90% of what was released;
- Lack of transparency of what's actually deployed;
- Release notes (and I can guess, also commit messages) not pointing to any user stories/tickets;
- Tickets being poor in description and being purposely vague;
- ...

Depending on your experience you can probably image more "sins" based on these.

This "grind my gears" and I don't have a lot of advice on this, but, I'd follow the same approach as before in these kinds of projects: after a couple of attempts to improve and change the project "environment" for the better of all involved, I'd just jump to the next project. Why? Because with my experience I've realized: there come times where you notice you won't change poor mentalities/mindsets, and your time is limited and better invested elsewhere.

## Wrapping up

To me, participating in the development process, in particular, participating in code reviews/pull-requests, "supercharges" my testing efforts. I might not be able to review everything. That's ok. But not having that chance, is purposely impeding me as a tester from doing a better work, and further developing my craftsmanship, and this cannot happen. Hence I "non-jokingly" said: on a good chance, I'd just pack up my things and leave.

In the limit, asking questions, in a matter that is traceable and documented towards the future (example: questions in a Pull request) is not a waste of any person's time in the long run - it's a good investment for the project. The project will inherently become more richer, because, maybe, with asking questions: some complexity was removed, or some problem got closer to a solution. It's not a problem.

Don't be afraid. Read. Look into. Review. Ask.