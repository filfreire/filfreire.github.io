---
layout: post
title: "Asymmetric warfare, raids, and software testing"
date: 2018-12-08
categories: [Raid-ST, testing, quality]
image: /assets/images/2018/12/cod4.jpg
caption: "Call of Duty: Modern Warfare Remastered, 2016"
---

> "The world is in great shape (...)" -- Gaz

Everything needs to be incredibly faster everyday. Decades have passed and the difference between quality control, quality assurance and testing is still a whisper in the wind. The world is set on hiring people to magically assure quality (whatever that is). Terms like "automated testing" (which should be called checking) gain traction.

## The problem(s)

The industy is hungry for testers. They want them in every "shape and size", most of the times with the same (vague) profile descriptions: "we need someone who can write testcases" "we need someone who can use a ticketing-system and a testcase-management tool" "we need someone who likes breaking stuff (* - but isn't the stuff we test already broken?)" "we need someone who can automate tests in language X" "we need someone who knows everything about test framework Y".

Any tester, after successfuly passing through the above checklist, will maybe set up against:
- Projects run by dumb person(s);
- Projects run by dumb mindset(s);
- Complex projects;
- Confusing projects;
- Risky projects;
- Scope-always-changing projects;
- Scorched-earth projects (something happened that people in these are already burned-out);
- All of the above.

In all projects though, good and bad, there's usually a prevalent point of contact for most testers: Asymmetry.

## A landscape of Asymmetric Warfare

There's always some "big monster challenge" and the "testers are so small" and budget is to tight for more testers. Better yet, maybe tons of developers are churning out tons of code for the same project. And to add to the cake, all of this code in under a spell of "no rigour", no unit checks no code quality, stopper bugs being found all the time. Codebases built on dress-the-shirt-long-nighters by cowboys with spit and NASA-duct-tape, conveniently and easily deployed in the cloud for a modest price (tons of money... and some dignity). Cool and hip slopyness reign.

And what are some of the common ideas to top sloppyness?
- "Let's create tons of test cases";
- "Let's create a big and costly and hard to maintain automated check suite";

<figure>
    <img src="/assets/images/2018/12/borat.jpg">
    <figcaption>Borat, 2006</figcaption>
</figure>


There's much to be said about what I've just wrote above. But stop and think for a minute. What kind of tester do these projects really need? Under what the context do the ideas above work to magically solve sloppyness?

Let's say we're faced against a big monster project from the required testing efforts point of view. First problem we face is we won't be able to top up the monster: there's not enough testers in the market available at this very instant. And if there are (testing sweatshops), it's a big risk: it's a cavalry made up of (possibly good or possibly bad) mercenaries that's setup to be called late and to arrive late.

If what we have is asymetry: we desperately need some asymetry warfare tactics. So...

## Introducing "Raid Software Testing"

Yes, it's not a typo, I didn't mean Rapid Software Testing. I'm nicknaming it Raid-ST. It's inspired by RST, but it doesn't aim to be any sort of substitute to it methodology-wise. Both can work at the same time, and at best, Raid_ST it kind of a guerrilla-branch of it born from being exposed to the ideas of RST.

There are only 3 main points, in The Manual of Raid-ST:
1) Context-wise, you need to have a monster of a project (discussed above);
2) You need to gather skilled Tester-Commandos (who can do the right amount of skilled improvising on the job);
3) You send the Tester-Commandos on Raids (quickly coordinated "airborne" testing efforts effective to a certain degree aggainst all kinds of testing challenges (targets), or quality assurance and control deficiencies).

### The concept of Tester-Commando:

Skilled tester-commandos are testers who:
- Love learning, asking questions, and studying;
- Care about their craft;
- Care about others;
- Have decent coding/scripting skills;
- Solid foundations in software testing, quality assurance and quality control (actually knowing the difference between the 3 is a good starter);
- Have decent foundations in various concepts in software engineering.

Ideally were talking about testers who can easily tag-team with developers or managers to unblock any kind of situations, but that can also in fact perform great testing.

Easier said than done. But indeed I've noticed a pattern everywhere I go: testers are always at some level in the "Commando" scale, with different strenghts and weaknesses, which directly impacts their performance in the projects they work with (depending on the context of the projects).

I feel from experience that Tester-Commandos are more appropriate for a certain kind of "monster projects", specially at a stage where testing efforts and quality processes in those projects are very poor. So the idea is that these come in, introduce some meaningful short-term changes, and after that, you can call the cavalry of other profiles of expert testers to really make a deep and impactful long-term change.

### The concept of Raids:

Raids are not long-term test plans. They're (apparently) simple but not over-simplifying in terms of purpose. The're also not set to be ineffective: a minimum effort has to return at the very least some value.

Here are some of the possible purposes of raids:
- Moralize and educate the team to follow apropriate testing methodologies;
- Elevate the tester's role in the team;
- Capture and convice specific key persons or stakeholders attention and hearts towards testing challenges through thoughtful testing;
- Gather and organize as much intelligence as possible (be it laying out documentation that the team can use, documentation that testers in specific can use, or setting up meaningful automated checks and reporting patterns);
- Lay down some foundational ground work that other testers can lean over in the longer-run in terms of test strategy, test plans;

Here are some other possible purposes, not directly related to testing, but that a Tester-Commando should be able to do:
- Moralize the team to follow better code quality practices;
- Introduce good practices, via actual examples, in the codebase (unit checking, code analysis, code quality, ...);
- Destroy the "status quo" and current "installations" of mindset "no time to create unit checks"/"no time to document";
- Helping developers and testers get free-er from the grips of blame-driven/guilt-driven management, by educating them for example on how to better communicate their doubts, certainties, and guesses;

All of this can be done in separate or with some mixture. Expert testers will say I'm taking a road of potential "blasphemy", and that I might be riding a dangerous train of thought of mixing Quality Assurance, Quality Control and Testing Craftsmanship, acting as a "counter-revolution" voice in the dialog between the factory school of testing and the context-driven school of testing. I admit it appears to look a like mixture, but with the intent to be a purposeful and heterogeneous one.

The idea of Raid-ST is not to be a unique flagship of testing expertise, but rather facilitate the introduction, "later in the war", of expert testing, while ALSO contributing towards decent quality assurance and quality control processes (which may also facilitate expert testing efforts). In other words, it's like a first layer of "violent hygiene": the main premise is to debilitate "the monster" in a methodical yet "portable"/easy to deploy way, so that, for example, later efforts can be made into having even better testing happening in the project.

<figure>
    <img src="/assets/images/2018/12/RaidST.jpg">
    <figcaption>A visual representation of Raid-ST</figcaption>
</figure>

## Eating my own dog food

I've been asked on several ocasions to jump inside a project, help out and improve testing efforts and quality processes, then called to move to the next more-complex project that need help and fixing, and so on.

Much like a commando that is pin-placed in the hardest parts of the world for a very limited ammount of time with a clear set of objectives, once those are done: time to evac back to base, catch a small ammount of rest, and of again to a new mission.

Because I have to be on the move, and I can't be in all places at the same time or clone myself, I usually have to make a lot of bang with the instruments I have at hand.

Much like the intro for the british mission on BFV: "it's always a job that requires a certain ammount of thinking on the job."

 Between critical projects there's only so much "instruments" I can carry with me:
- My laptop (with a set of software tools always installed, see /onboard), plus books, cables, and phones, if applicable;
- Some contacts which might help me unblock tricky situations (like infrastructure setup, permissions, finding other person-of-contact people, ...);
- My previous tacit experience from previous testing endeavours, which is somewhat intagible;

I also always leave behind certain beacons, or "care" packages, in case I ever need to get back to the same place:
- I document everything that I tend to forget;
- I document everything that a future version of myself might need
- I document everything that up until then hasn't been, but the team gains from it being documented;
- I automate boring parts of my endeavours;
- I version/source-control this automation of boring parts work: I always carry repositories with tens of scripts to bootstrap/quickly set up camp again, in case my laptop dies, or I need to assist the project again, most of which help me on my next projects;
- I build as many relationships as I can, in case I need help with things I'm not an expert with.

And finally, in every project, I always attempt to start (and finish) **Raids** (typical purposes are the ones listed above), here are some examples:

- Evaluate the status of code quality of all repositories, and see what is both achievable and important that can be added as part of the code quality processes;
- Fight the myth of "no time to test"/"no time to document";
- Evaluate the status of continuous integration in the project and make improvements where applicable;
- Automate dumb but important stuff;
- Learn as quickly as possible from other testers in the project what are the current hardships, and act on them;
- Participate in the code-review processes, suggest and contribute unit checks;
- Perform Survey and sanity testing, report as many important bugs as possible;
- Create product coverage outlines from day 1;
- Help out other testers making better of use of their time, converting time wasted in "administrative tasks" into time invested in actual testing;
- ...

## Summing up

Reality check: Not all Raids suceed, even if producing a bit of "damage" to the monster. Sometimes they end-up badly for the operator too, so I underline the importance of adapting the right raids to the apropriate context. When the Raids fail, a tester-commando can and should quickly try other raids.

I'm personally far from being a flawless example of tester-commando, much less of a real-life commando. I tried though to put into words and explain my personal methodology, which anyone who knows me in real life also knows I fall short-of. I'm a flawed human being, and that's ok.

If I conviced you or gave you some ideas with Raid-ST, awesome. Come back later for more adventures on Raid-ST :)

Far from trying to convince anyone to adopt Raid-ST, which to me personally sounds a bit silly, I do make this invitation: Recognizing your own personal methodology, studying it, and trying to improve it on a daily basis can take you far, and definitely is a force applied in a daily pursuit of paths less-traveled. It's worth it.

As a motivational outro, if there's one thing I'd like you, the reader, to take from all of this is: try a bit harder, and think, and do something with discipline. Your mind is free. If I managed to write all of this down, I can't imagine what ideas some brighter minds are on the brink of putting into words, but need that spark. Here's a spark for you.
