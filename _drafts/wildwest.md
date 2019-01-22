---
layout: post
title: "(Early DRAFT) Wildwest rules"
categories: [draft]
---


Recently I came by this comment made by someone working in some tech company:

> “(...) but the tech lead will not allow testers have a look at any code.”


I instantly felt triggered, offended, and whatever it is that people say to express how horrible they feel with something that seems "unbelievable".

This is a "no brainer" for me: I’d happily leave that company asap.

Unless the code involves launching of nuclear missiles or some top secret confidential national security stuff (and even then…), I expect the same kind of access to it as a tester, as any contributor has to an open-source project: I want to see the code, the logs, the different environments, the discussions, I want to have the ability to investigate everything and anything that will influence my testing efforts.

Recently for example another colleague shared an article on a Slack group a link about ["whether it's important or not for testers to have the power to read pull requests"](https://dustyjuhl.com/2019/01/14/is-it-important-for-testers-to-read-pull-requests/). For me this is not even a question. It's not a matter of being important or not: I consider it a part of my job, and a crucial tool in studying implementation and, as mentioned also in the above article, it's a shortcut to indentifiying some category of issues very early on the development process, earlier than that being "contesting" a development's specification even before a developer grabs it and starts working on it. Again, it's a "no brainer".

TODO

## But what of the testers that can't read code?

[Can't they? Really?](TODO - james post about non-coders/video). This is a falacy and also it's fake news. Unless you're an non-coder european reviewing code that was done with Chinese or Japanese characters, if you can read english, you can review code. You might not know how to code, or the intricacies of the language, but you certainly know how to ask questions. So what's the problem?
Almost all programming languages are "english", and interpretation of the code is not that difficult: you get the "idea" of things, so you can ask a question when you spot something weird. And when you don't get the idea or get the wrong idea, again, you can ask.

Some may say: But these testers asking me stuff is a nuissance!

Yes, at times. We need to build a good relationship with developers beforehand, because the nuicanse is there even for testers who are coders and fully understand the code: some developers don't like to be asked questions by anyone. This won't change any time soon, and will happen in every single project, guaranteed.

But not asking anything at all: that's plain dumb. It's not using a valuable pair of eyes with not context on your solution to mentally "put their finger on it" and see it in a perspective you haven't seen it as a developer.



## A sin is never alone

But this matter of "secret pull requests" was not the only "sin" of this colleague's "architect/tech lead", the usual sins carried on:

- Release notes missing 90% of what was released;
- Lack of transparency of what's actually deployed;
- Release notes not pointing to any user stories/tickets;
- Tickets being poor in description and being purposely vague;
- You can probably image more sins based on these...

TODO


## Wrapping up

To me, participating in the development process, in particular, participating in code reviews, "supercharges" my testing efforts. I might not be able to review everything. That's ok. Not having that change, is purposely impeding me as a tester from doing better work, and further developing my craftsmanship, and this cannot happen. Hence I "non-jokingly" said: on a good chance, I'd just pack up my things and leave.

In the limit, asking questions, in a matter that is traceable and documented towards the future (example: questions in a Pull request) is not a waste of any persons time in the long run - it's a good investment for the project. The project will inherently become more richer, because, maybe, with asking questions: some complexity was removed, or some problem got closer to a solution. It's not a problem.

Don't be afraid. Ask.