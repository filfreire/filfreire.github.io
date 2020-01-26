---
layout: post
title: "Why did I miss it?"
meta_description: "Why did I miss it?"
date: 2020-01-26
categories: [testing, personal experience]
image: /assets/images/2020/01/stranding.jpg
caption: "Death Stranding, 2019"
---

> "There is an evil I have seen under the sun (...)" -- Ecclesiastes 10:5

Today I want to talk about an "evil" that plagues a lot of software companies (or companies that do software?): when testers miss bugs.

What? Are you serious? Impossible!

Yes you've read it right. But this "evil" is not alone! It's usually so malicious of an evil that it poses an existencial problem for career testers: 

> "my senior leadership (usually the boss of the boss of the ... of my boss) or even said "normal" users (most times on social media) are finding more bugs that supposedly I'm paid to find!"

And then the Gorgons of the software world jump in and add to the mix: "You're paid to assure quality!" and then promptly turn you into stone.

I've seen it happening time and time again, and where I fall short in terms of "years" of experience to have seen it in the old days, I sometimes have heard of the same tragedy dramatized by "folks who came before", our beloved dinosaurs in tech.

But, there's good news: This evil, as unpleasant as it might be, is not impossible to beat. You can always hit it with a rolled towel.

Let's look at what is actually happening for this nefarious situation to have had birth. I have a possible explanation:

## The "vile" investment

Sometimes, if we're honest to our heart, it really turns out that the senior leadership and normal users are, without putting much thought into it - actually INTERACTING with the end-product, in ways any human would. Be it in expected, unexpected ways, or even malicious ways - at the end of the day, actual users do what actual users do - they interact. They inadvertently learn. They experiment. They uncover the facts.

And meanwhile, maybe, just maybe - your testers are invested in maintaining automated checks, test cases, test documentation, reproducing “test scripts” manually, “testing regressions”, etc etc - stuck always on the same spinning wheel. They have their minds so busy with all this "maintenance" stuff - that at the end they spend on a practical way - less time interacting with the product in a meaningful way - than a user or a senior leader that just decides - "hey I want to do this, lets use the product for 30 minutes”.

The same happened to me a lot in the past, and rightfully so - at the end developers and others could perfectly say to themselves: _"but Filipe why did you miss this? Why are you not testing? You're a bit incompetent a tester don't you agree?”_

Ouch.

I’m the first and main person to blame - the truth is quite simple, I wasn't testing. I was doing all this other "pretty and useful" stuff that wasn’t necessarily testing… usually it was maintaining automation, or test documentation, and maintaining or creating “dummy”/“meaningless” evidence of testing. And one can be awesome and great at doing all of these things - but they are still not a replacement for meaningful testing:
- Meaningful/purposeful interaction with the product;
- Learning, asking questions, hunting for confusion and risks;
- Experimenting all the way!


## A moment of self-reflection

I'm constantly learning through my many mistakes that there's a moment in time for anyone to turn "the tide".

In this particular matter, it all comes down to having the guts to ask yourself as a tester, or a test manager, or a tech lead, etc: why is it then… that a senior president that invested 5 minutes with the product… is finding stuff that I or hundreds of my testers missed?

> "Uh, Uh, I know, we need more test cases! No, no, we need better test cases! We need to cut minutes in the automated check pipeline! No, no, we need to use a different library! No, wait, let's make the developers help in coding more automated checks! Let's delete the automated checks suite, and create a new one! ...."

If you follow that line of thougth, my friend I have to warn you, there's always something to do or improve or get lost into, most of it seemingly fabulous stuff that is using latest trend and fashion and a standard so clean and shiny you can see your face reflected on it. But you'd still be missing the point.

There comes a moment in any of our lives as "testing people" where we have to be beastly enough to ask "Maybe me or my testers are not investing the better slice of our time in stuff that actually matters: testing".

It's a punch in the gut for sure. But time and time again I've reached this realisation by observing the same evil in it's different shapes and forms: When you're missing the main target, that target will hit you back eventually.

## Switching sides then...

So you're past the self-reflection, what do you do next?

Well the answer is simple. Stop what you're doing, and get to work. You need a new "baby".

> "But what about my (old) "baby"? I can't leave it behind!"

Leave it. Whatever your "tech baby" is, it's ugly. If no one told you that yet, tell it to yourself, and move on. 

It’s one thing to have someone whose job at the end isn’t “testing” ending up doing testing - and then it's a whole other thing having someone who is a craftsman tester in your team with the headspace and resources to invest their time testing - because then there’s a difference, it’s a chance at meaningful deep testing that completely smokes the usual “passive approaches” of:
- “I want to maintain tons of test cases";
- “I want to see all my testing evidence in beautiful graphs of percentages and numbers of cases passed and automated";
- “I want to automate testing";

And before you misinterpret the above:
- Testers can indeed spend half of their time coding automated CHECKS - its not bad, it’s a good option. Testers and coders who do it are amongst the best testers/coders out there;
- We can automate checks, test data generation, deployments, and so many other things - they’re useful and valuable - it’s always a good and worthy endeavour;
- Testers should be encouraged to create meaningful and insightful documentation and do maintenance work - as long as it's balanced with their main mission which is to test... if otherwise it's getting in the way, it needs a pulse check.

But, on the other hand:
- Using _“automation”_ as an empty word of order to help justify one’s poor test strategy (that involves zero interaction with product) is a crappy option;
- The vague _"I serve to assure quality"_ mission statement is a path to foolishness - guess what, your boss's boss just called, yeah he just found something ugly in production while you were busy doing the "quality babble" dance;
- Getting lost in a "cycle" (strategy) that is not returning any "value" to your project, and then deciding to do a "new revamped and improved" cycle, usually from experience means you'll just get lost in another crappy (but "prettier") cycle;
- Using any sort of documentation, numbers, or maintenance work as the main reason of "existence", and then using it as evidence of "quality", is always a downward spiral.

The first steps are the hardest, often inarticulate, and to it's core they're all about leaving behind ways of working that have become through time part of our own self. But once the first steps are taken, then the awareness slowly starts kicking in.

Sadly, I don't think there's "one-formula solves all" after the first few steps. Your journey is yours to travel. People usually invest a lot in the craft afterwards. They look with thirst for other people who are masters in the craft. They long for becoming better testers, using any methodology that fits best their context, and are eager for learning more and more.

There are also signs you can look for:

- You're more confident about your limitations, you embrace them. Oftentimes you slowly become more compassionate of others;
- You're less afraid to tell people who don't know anything about testing that they can depart back to their hole, be them colleagues sitting next to you or entire self-proclaimed "Jedi Councils" or "United Nations" of testing;
- You embrace confusion and complexity, knowing that they are necessary companions on the road to grasping the testing craft;
- People around you start noticing that you're raising issues, confusion and questions that actually matter to the people who matter;
- You're the go-to person, not for "a green light" or "go-no-go", but for a conscious diagnosis of the product at any instant in time;
- You're useful. The bugs that end-users find, start to become more a culmination of points where your _"sight isn't sharpened yet"_, and not a plain symptom of _"in practice, no one was really looking"_.
- ...

## Wrapping up

The "evil" will not go away unless you as a tester send it away. And sure enough, it might be offensive for many to remove that "evil", but be honest to yourself, do you really want to invest in a structure and aproach that is hogwash? If you do, then don't be surprised you or your testers aren't doing the best of their work. Sure they might be doing amazing and beautiful things, but it's not testing.

It would be the same as telling your loved one a thousand times you love them, but it won't mask the absence of practicing that love, and being insincere by then going on to do things that are not loving that person back in practice.

Is your Chief or the user next door finding problems everyday? Then maybe your approach to testing is an overstatement, if not inexistant in practice. It's time to wake up!

Thank you for reading. Feel free to reach out to me with comments, ideas, grammar errors and suggestions via any of my social media. Until next time, take care!