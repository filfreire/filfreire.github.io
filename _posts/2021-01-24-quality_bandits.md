---
layout: post
title: "Quality bandits"
description: "A look at grifting in corporate Software Testing"
meta_description: "A look at grifting in corporate Software Testing"
date: 2021-01-24
categories: [thought piece]
image: /assets/images/2021/01/catchmeifyoucan.jpg
caption: "Catch Me If You Can, 2002"
---

Here's a curious thing I've been thinking about these past few days... If you work (or have worked) in a modern tech corporate environment, you might have run across this particular scenario.

Picture a few top brass folks, typically folks that don't care for testing, but for the variables of this scenario let's not even consider that bit, they all gather up and proclaim:

> "Let us devise an initiative to reduce the number of defects in production services!"

Stop here for a moment. What would you do in such a situation?

Did you think about it? Are you ready? Ok, let's go on.

I'll tell you a secret - it doesn't matter what you thought about so far. You see... the top brass folks are already convinced of what they need to do. They did a `TODO` list of fancy corporate lorem-ipsum things like "standardize tooling", "standardize results", "automate as much testing as possible", keep track of everything in graphs, measure pass/fail values across the entire company, label and enforce a standardized structure on bug reports, and "strongly encourage" QA folks and their teams to increase those pass/fail ratios, and increase the amount of "quality metrics" they expose. All in a standardized way so top-brass can assign KPIs to it. It doesn't matter what those KPIs are. They will likely be cryptic and meaningless.

If you know me personally, you already know what I think about most of the aforementioned hogwash. But let's try and be constructive for a moment, and offer an alternative. I've gone way to many times into the rabbit hole of why these folks are acting stupid, if you want to go deeper on that, you can read more in posts like [this big boring one](https://filfreire.com/posts/quality_infotainment) and [this other one](https://filfreire.com/posts/why_did_i_miss_it).

## The scam

There's a reason this mindless "_jump to action_" of these folks is oftentimes the case. My personal running theory about it is:

> Their minds and ideas and concepts about Software Testing and quality have been victims of grifting.

"[Grifting](https://www.dictionary.com/browse/grift)" in the sense that they've been "victims" of fraud and scams (oftentimes self-inflicted) when it comes to looking at Software Testing problems.

These same big bosses that are quick to try and "_sooth the waters_", and seemingly care about "quality" and take every public opportunity to voice their concerns on "quality", they all make the same mistake: they attack the problem of "_our apps/services/infra are in a fecal state_" by fooling themselves and others in tackling the problem with brute force (brute as in ignorant, barbaric and belligerent) instead of actually taking a step back and thinking about the testing problems they have at hand.

The ruse, which you might be able to observe in corporate environments where the testing culture is poor, turns over time into big balls of mud:
- the initial gain of trust: "_since we appear to be moving towards a goal_... _we must be doing good_";
- the build-up: the increasing dissonance of "_the initiatives we are doing_" vs. "_how come we haven't affected the cycle of embarrassing bugs and problems?_";
- the "hurrah!" moment: tragedy, failure, embarrassment and someone renews the cycle, recycling the scam.

## Alternative path

I can tell you what I would do. I would stop the buck in its place and do the one thing that a lot of these top brass folks are forgetting:

__I would (try) to look at the problem__.

There's just so much to tidy up on the problem before we jump at solutions!

Let's look at the "technical" part of the problem first:

- If there's an underlying feeling that we need to reduce defects/bugs - why is that? Do we have too many bugs? Do we have a lot of embarrassing ones?
- Are the embarrassing bugs being found first by top brass folks or our common users?
- How respected are Testers in the organization?
- Are our Testers overwhelmed with bullshit bean-counting work?
- Are our Developers minimally responsible and check their own work?
- Does the organization understand the value of meaningful testing?
- Does the organization value testing (practical e.g. - it knows the difference between Testing and Checking)
- What do our bugs look like?
- How TESTABLE is what we build?
- How STABLE is what we deploy into?
- What is the development process like? Mature? Crappy?
- How empowered are Testers to spend the most precious chunk of their time doing actual testing?
- How empowered are Testers to test complex flows?
- Are tools an imposed hindrance or forever-patient and accessible?
- ...

Then there are often other factors, the old _"where are all the dead bodies buried"_? Let's look at the "human" part of the problem:
- Are folks victims of workplace bullying, sexism, racism, homophobia, transphobia, ...?
- What are the actions (if any) to SOLVE the above issues... excel sheets and "mandatory" diversity virtual trainings?
- Are good folks leaving? What was their feedback when leaving? How are we accounting for that feedback?
- Do folks have an actual living wage and subsidies where applicable, e.g. during home office "corona" times do we pay them extra subsidies to help with home expenses, or we make them feel guilty for not being in the office?
- Is hiring and career-progression human/humanistic?
- Do promote/celebrate folks that deliver working (and valuable) pieces of software?
- Do folks have creative freedom and do we respect their personal & family time?
- Are top brass proclaiming weird stuff like "_during these times, we need to be careful not to hire burned out folks_" while being surrounded by scorched/charred/scalded colleagues?
- Is the org run in autocrat fashion, with forcible suppression of any practical opposition and strong regimentation of everything?
- Are most new entries of senior leadership serviceable only for the duration of their probation period, and mysteriously disappear, "_in effect immediately_", say, by means of "_retiring_", "_personal situations_" or "_adopting new challenges_" ?
- ...

All of these questions (and many, many more) help paint a picture of the organization, and serve as a map for software testers and developers alike. You may have narrowed down the options to solve your Software Testing problems in your organization through some of these answers. Experience tells me, the solutions rarely look like the ones the typical brute force approach described above entails.

I invite you now to take a moment to think: have you ever seen a top-brass person deeply search for answers to any these questions before tackling a Software Testing / Quality problem? If they didn't... did they give empty excuses?

I'm posing these questions because, from past personal experience, if I gave any "low brass/ grunt" colleague a "pen and paper"... they would often be able to answer almost all of these questions truthfully in less than a few hours, BUT, the actual competent top brass folks that reached out and cared for stuff like this, I count to this day with the fingers of one hand. Maybe just my personal experience, who knows, right?

## Wrapping up

Long story short: Trying to solve a problem like "_reducing number of defects_" needs, first, more than a blind _jump to action_, a careful review of the context one is in. Listen to your Testers. Listen with critical ears. Otherwise, you will play yourself, seduced by the siren song of "_control of quality_". And somewhere, trust me, a grifter is filling their pockets. [Such is life, some would say](https://www.youtube.com/watch?v=L_jWHffIx5E).

<center>The path to less problems in Software Testing, is the one where we are hunting for more of them.</center>


<br/>
<br/>

________

_If you read this far, thank you. Feel free to reach out to me with comments, ideas, grammar errors, and suggestions via any of my social media. Until next time, stay safe, take care!_