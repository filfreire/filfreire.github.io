---
layout: post
title: "Metadata of starting"
meta_description: "Metadata of starting"
date: 2018-09-24
categories: [thoughts, craftsmanship, testing, quality]
image: /assets/images/2018/09/toy-story-staff-meeting.jpg
image_alt: a movie still from Toy Story, 1995
caption: "Toy Story, 1995"
---

> **TL;DR**: When starting at a new project as a tester, be on the lookout for meta-information that says a lot about the project and will help you guide your testing, but is typically not apparent, as so, it has to be unpacked with a detective stance testers should practice.

Sometimes as a tester you'll be faced with switching between completely different projects with multiple different realities and associated contexts. Depending on who you work with or if you do consulting, this reality and project switch happens abruptly and you're expected to quickly adapt and add as most value as you possibly can via testing efforts that somehow will need to emerge from unexpected and uncoordinated testing missions.

We feel confused, and in the midst of confusion we allow ourselves to create quick "shortcuts" of reality:

> "Oh this projects seems bad! I hate it!"; "Oh this project seems awesome, I love it!"; "The people seem grumpy and unfriendly..."; "The people seem nice!";

Adding to that, we feel completely lost. Like we've been piloting small airplanes our whole life, and in one instant we're forced to pilot a boat with a complex console. But, contrary to the negative emotions we allow ourselves to develop even further into more negative emotions and thoughts, feeling lost is not bad.

For anyone feeling lost and confused, it seems like it's the end of it, even before allowing a chance for anything to start. Times come when we've already given up. It might take years until we try to do something about it, but the decision to give up was long ago taken by a past-self, someone who we no longer recognize.

You might be wondering, what point am I trying to make here?

## The illusion of confusion

Confusion in a software project and in life itself is not bad. Much less for a software tester inside that project. Your testing efforts shouldn't start with "Despite all of this confusion, we still managed to do X". They should embrace confusion and pick on it.

Look at it in another way. Confusion and being lost tells you more about the project you're put into than you're mistakenly led to believe initially by your feelings and observations. Starting at a project is the perfect moment for tremendous information gathering, analysis and experimentation, way beyond your initial onboarding process and the onboarding's confines, and way outside the scope of what is initially apparent. Starting at a project should be like a royal hunting season for a thoughtful software tester.


## Asking questions

I've come to develop through time some questions that I ask people directly, or I just try to build an answer from observations, talking to people, going through code, documentation, code reviews, and other, that I believe allow a tester to cope with confusion (even generating more of it, but that's fine!) and make a difference when you're trying to be crafty and help the project as best as you can, as early as possible.

There is no right or wrong answer for almost all of these questions. Every bit of information is a bit that will potentially guide and help me adapt my testing strategy and efforts.

I've compiled here a list of some of them, that I usually go through, most times in an unscripted way. All of them have the goal of peeling bits of information about the project, and I invite you to read each one, think about it a bit and try to think how you'd answer it in your current project, even if you don't get the point of the question:

- **Do you think a bug is a good thing or a bad thing?**
> Let me explain this one with a bit more detail: It might seem a dumb question, but it's not a simple question. When I ask it, I'm more interested in finding patterns that can be picked up on the other person's answer and I've found it tells a lot about what are the person's priorities in the project, what's the underlying view the person has of the project, and also how much respect the person has for testing craftsmanship.

- Do people in this project **truly know what is testing**? Do they know the difference between testing and checking?

- **Is testing respected or it's really nobody's true focus?** Are there figures inside the project who aren't testers but enforce their distorted vision of testing to other people?

- **Are people used to have their testing challenged?** Are there any craftsman testers in the project?

- Is the focus of the project on deep testing or is it on shallow testing? Is it a blind focus?

- Do people clearly have a grip on the ideas that guide all their testing efforts? (a.k.a, do they **know what's their test strategy?**)

- Do they have **strict code quality**? Is there a **balanced code coverage** of testable code and the logical complexity of the crucial parts of code is at the very least picked by reliable unit checks?

- Do people **have fantasies about tools**, automated regression suites made up of old checks (not tests) that will magically prevent bugs from ever coming into existence and are a replacement for exploration and experimentation made by a thoughtful and skilled (and possibly tool-savvy) human being?

- **Is the documentation** simple, but not over-simplifying, and is it **alive, healthy and maintained**? Is documentation considered unimportant or not worthy of respect in critical or poorly-managed times?

- Do people stick with some **self-created and self-imposed pseudo-Agile dogmas**? Are there any fervourous adepts in the team of the "pseudo-Agile-move-things-break-fast-dress-the-shirt" religion?

- Is the development/integration/deployment process a lie, or contains a set of lies?

- Do people fear other people in this project? Do people fear thoughtful testing, or even fear to report any issues openly?

- Do people freely communicate? **Do people over-communicate?** Are the communication channels in place dumb/noisy/clear/straightforward/enough?

- **Is the project traceable?** Is everything traceable?

- Can a junior developer clone a repository and submit a solution to a simple/minor bug in less than 30 min on his first day on the job? And can the fix be easily deployed to a test environment tested on a deep level?

- Can the same developer do the fix on his own without nothing but access to the internet, the code, and the project's documentation, all the while **without asking** the senior developer the same questions every new junior developer asks every time they join the project?

- Would the previous scenario change for a more complex bug and a newly-joined senior developer?

This list goes on, I can think of more questions, but these are the ones I keep coming back to eventually.

## Now for the final trick...

Some of these questions are __plain dumb__. Some of them are __harsh__. Almost __all of them are biased by my personal experience__ and path in the testing craft.

But, the final trick is: **the questions don't really matter**. What matters is asking questions. What matters is fighting confusion with a detective attitude that every tester should nurture and grow. You fight confusion with questions, with problems, with bugs found, and with even more confusion.

The underlying goal is to develop the healthy habit of quickly gathering as much information as possible during the initial moments of a project, even information that at first hand might seem unimportant. I'll get whatever I can grip regarding the project I'm placed into, because this "data about data" also guides my testing. And I'll do it with these questions and many others resources.

On an ending note: If you never learn to love and embrace confusion in software testing, you'll never feel the true joy of testing. To joke a bit: It's the same as being a tomb raider while disliking and avoiding tombs.