---
layout: post
title: "Teleporting to conclusions"
meta_description: "Teleporting to conclusions"
date: 2019-09-25
categories: [testing, personal experience]
image: /assets/images/2019/07/shooter.jpg
caption: "Shooter, 2007"
---

A lot of times when doing hands-on experiential testing, or preparing data for a load test, or even reviewing and coding unit checks I find myself jumping to conclusions.

The explanation of the psychological term with the same name goes about something like this:

> "communication obstacle where one "judge[s] or decide[s] something without having all the facts; to reach unwarranted conclusions" ([link](https://en.wikipedia.org/wiki/Jumping_to_conclusions))

Often when testing I don't have all the information or all the facts. I'm most often hunting for them, based on observations and assumptions, using testing as a vehicle to find information about known unknowns, risks, and even dispell illusions I or any other member of my team has.

But there's trouble in this: by being solely based on my assumptions I'm not setting a "perfect" course nor am I going about with silver bullet material to start with. I end up directing my testing efforts oftentimes unknowingly (or distractedly) setting myself up to stumble upon unforeseen troubles, unknown unknowns, or even apparent issues that become apparent, say, in the production deployment of what it is I am testing at any moment for example.

## Examples of stumbling

### 1) The apparently hidden characteristic

A lot of times specifications or acceptance criteria, or whatever it is you want to call it that seemingly helps you give boundaries to a problem, miss out on implicit criteria and implicit ideas that are held by different "actors". Even if one is not a very creative person, almost all planned (and unplanned) chunks of work leave some room for interpretation and implicit understandings, which then lead to the stumbling of apparent things which looked hidden.

Confusing?

Say we're looking at a problem through a set mind, looking at what's apparent. The problem is something as trivial and ambiguous as the one below:


> "Think of a grid-like figure made up of similar polygons, among these: squares. How would you get to the number of squares in any grid-like figure?


(I left the problem description ambiguous on purpose - though you can find flavors of the problem above better explained on some online videos...)

In such a problem, typically most people would stop and ask for an example before going on, to be able to visualize: which is reasonable. Or people may want to ask more questions to get more information. One might be tempted to count only the smallest of squares. One might be tempted to count the squares that are made up of smallest of squares as well, but not easily visible. Some other person will also count the squares that are made up medium-sized ones, and so on. Some will count rectangles in as well, for some superstitious reason they can't quite remember, but has to do with something the Maths teacher told them years before.

Each of these people trying to solve the problem above might believe to the core of their being they are looking at the problem correctly, which ultimately doesn't matter - if the criteria for solving the above problem leaves out this information, leaving room for interpretation and wrongful approaches towards solving the problem.

This is not different in the software development world, no matter how much specification we put into a chunk of work that some programmer is expected to finish in a given amount of time, and the tester to magically test "quality into it" (yuck!) in a matter of a few minutes. An often overlooked piece of the puzzle - a developer is also oftentimes in a discovery process, implementing something to figure out something like follow-up specification itself or some other hidden obscurity that isn't there until one delves into code.

This particular "Jump-to-meaning" ultimately leads to all involved (including Testers) to forget to look at a given problem with more than one perspective, which later on causes problems that would be otherwise apparent.

I don't think there's much of a recipe to avoid this, aside from taking initial and subsequent observations for what they're worth.

### 2) The unforeseen function

This is one of my favorite existing ways to stumble: Following the clearest and "most important" user paths, forgetting that in the same context, any minimal user path could be an entryway for malicious usage, and is as important as the "largest-user-behavior-fitting" paths, hence missed it during initial testing.

For example: how many of us testers and developers all include login and then some internal model instancing/creation in our automated checks? It's something prevalent in any software project that has automated checks - we'll have quite a bit of checks for data "creation/insertion". What we might often miss is, no matter if that data creation is human facing or coming from a contract with another service - can we trust the contract will be kept?

Certainly for the normal automated checks to pass the contract will be obeyed. And maybe the boldest of us will put quite a lot of work into input validation. But what of the actively malicious usage attempts by a motivated attacker fixated on exploiting and attacking our system/service under test?

Something as simple as considering that no one will sniff our application traffic and figure out the API calls we're doing, or no one will attempt API paths for data creation that we've only hidden by not documenting them or showing them - all of this is setting oneself up for being a victim of one's vulnerabilities.

It's best not to assume any client-facing API will be free from weird or malicious users with obscure intentions. Speaking from personal experience, this still holds true in 2019 (and certainly beyond) - wherein my free time I've found and reported things like a seemingly bulletproof food service application for an entire European country is easily exposing all their private user data, or a continuous integration verification tool that is as protected from the outside world as a potato is from a knife, and many other examples, all these systems exploitable long before the developers who create them can figure it out, and way before even opening the OWASP main page on the browser.

### 3) The unforeseen load

When preparing different kinds of performance tests we usually commit two distinct errors: we fail to estimate ("magic-ball predict") user behavior, and we fail to grasp the idea that linearity of "scale" is unlikely.

Here's a practical example based on my personal experience: At one point a few months ago I had to rushedly prepare some load testing efforts for production deployments. I decided I'd do so by doing a few really small scale load tests. On a practical level I simply set up a few `bash` scripts, repurposed some other scripts and Postman collections I had, and pretty much just started pumping data into my target test deployment. I was absolute "drunkenly" confident in my mind that, given I had not a lot of time to prepare meaningful load tests, at different scales, maybe luck would be on my side, and whatever I might find with a "duct-tape and spit" approach would certainly and magically translate into reality in production.

The premise was, back then:
1) maybe I'd find problems, which is super useful;
2) maybe those problems would shed some light of some characteristic on a bigger load event;
3) and maybe I could assume or deduce from interpreting result data on the experiments I did, that the behavior with "scale" and remain similar;

To be fair, the first step went great. Since for the most part I was experimenting with what I usually tested differently, and at a bigger scale than usual, indeed I was able to unwrap a few meaningful bugs and problems. But then I made the rookie mistake of completely ignoring the other two steps. I was done for the moment and put any second thougths on hold on line 3.

Sure enough, not long after, I ended up dealing with unforeseen consequences in production. It wasn't even by much, just a tiny bit more load than I'd settled for while testing. As expected in this kind of story, the consequences went completely over my efforts, kicked me in the stomach, and I had a new set of new problems, throwing to the ground whatever excuses and "makeshift" solutions I might have settled for or contemplated.

Not only that, when studying the actual production user behavior, and how that translated into a lot of typical things like number of requests to a given service or latency of given API calls or even what was and was not cached: I was in for a lot of surprises that no one could have guessed, no matter if we had stretched our imagination to infinity and beyond.

At that time, to be fair, I ultimately failed to serve my purpose as a tester, in part by acting like a rookie, in part by stumbling and jumping to conclusions with regards to load, I ultimately failed to hunt down for risks, problems, and bugs that were out there waiting to be found.

But the story doesn't end there for this "jump to meaning".

I learned my lesson. No more excuses, no more bullsh%&t. I gathered and studied all information that I saw would guide me, quickly picked a proper load generation tool that would help me focus on the tests at hand (and not lose myself in useless things), and started mapping out the load tests I wanted to run, step by step, setting their scripts up, setting up the load generators, and then off I went. I soon realized most of it wasn't rocket science. Sure I didn't have the experience of some craftsman performance tester, but I chuckled and felt embarrassed, especially when I remembered the stories of my older self or some colleagues in the trade: the curious case of the tester that dives into excuses and says they're "preparing" load tests... for half a year. A serious attitude shift had happened in me.

By the time the next production deployment arrived - I was not taken by unforeseen consequences. I had experimented in so many ways and at so many scales, that I had a reasonable degree of a "knowledge base" and confidence of what could work in production, what would fail and even at a very implicit level, I knew the potential breakpoints and risks, and had them ready on the tip of my tongue. All that by being in a constant productive cycle of finding multiple issues related to load, helping fix those, re-running load experiments, and repeating the cycle.

In this particular case of stumbling, I advise anyone, especially testers who haven't ridden the "performance testing" bull: take nothing for granted and don't take the long "excuses" road. Get to work. When you reach the point you're, say, killing your target deployment, and you end up killing some shared server, quickly needing to set it back up so your IT/Infrastructure teams don't find out/complain: **you're nearly halfway there.**


### 4) "The same model of the same car means any car is the same everywhere"

This is probably the most prevalent example of stumbling usually held by either junior testers, or by all kinds of senior management and "delivery folks" who have a very narrow understanding of testing: the strong belief that whatever it is you test in a test/staging environment can be a strong "linear and confident" estimate of what you'll see in production. This is never the case for a simple reason: They're different systems.

Even with all the containerization and "infrastructure as code" one can set up, or no matter if they might follow the same structure and replication rule set to the tiniest detail: overall we're talking about different deployment environments, different 3rd party services connected, different persistence instances with different data (even if with the same version), different configuration, and different unexpected usage, among many other things which make the systems "the same", but at the same time, "different".

The worst mistake one might make is assuming that the systems are the same, or expecting them to be the same. That is not to say from now on we can be savages, and rule-less. No. We should aim and fight with teeth and nails for the systems to be similar and easily replicated anywhere as much as we can, and there's no excuse in 2019, with all the tools and libraries available to not try this. But, any thoughtful and alert team member never forgets, that we're always talking about unique instances of the same system. Nasty bugs often go unnoticed when we forget about this key detail, and when we trust logic to apply perfectly while forgetting that we are flawed, imperfect, and we build imperfect systems always.

My best advice: never assume two instances of the same system are equal. And if this sounds weird... well, you have some options, like maybe studying the [second law of thermodynamics](https://en.wikipedia.org/wiki/Second_law_of_thermodynamics), until it magically sits in your brain as equally, somehow, applicable to software.

## Wrapping up

This is the first part of a larger post I want to make. In the second part, I'd like to go over concepts of Tempo, meaning, other problems of skipping towards meaning. If you read this far, here's a potato.
Until next time, take care!