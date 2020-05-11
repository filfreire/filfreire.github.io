---
layout: post
title: "(DRAFT) On the futility of quality infotainment"
meta_description: "On the futility of quality infotainment"
date: 2020-05-11
categories: [draft]
image: /assets/images/jp_404.jpg
caption: "Replace this, 2018"
---

There's an evil that found it's home in a lot of software projects, be those produced in small or big tech companies, from startups to old corporations: quality infotainment.

[Infotainment](https://dictionary.cambridge.org/dictionary/english/infotainment) is _"the reporting of news and facts in an entertaining and humorous way rather than providing real information"_.

"Quality" Infotainment is in its core form: the production and maintenance of any (irrelevant) "quality"/"QA"/Testing related information, processes and efforts that are the direct antithesis (opposite) of meaningful testing efforts or a negative move towards solving testing problems. Typical examples comprise coming up with numbers, figures and initiatives to entertain a specific set of stakeholders in anything related to Testing, Quality Assurance and Quality Control (both of which are not Testing), while at the same time not solving deep ingrained issues with the way Testing is conducted in the stakeholders' software projects, and being often pushed in a cyclical manner, fueled by attrition and the promise that "this time things will be better, just look at these tendencies".

In my personal experience, when taken to a fetish point, meaning the effort to produce this infotainment is given blind priority over doing problem-solving that matters, is probably the most popular and simple form of sabotage of software projects from the Testing (and Quality) perspectives.

There is, I admit, value in information, and the collection and presentation of __relevant__ information. Not a day goes by without me writing some form of test reports, bug reports, automated checks, and anything similar. The emphasis being always: what problem is this solving? Does that problem matter in opposition to other problems? Am I telling the truth, or exposing facts to people whom those facts matter? __Relevance.__

And you see, __relevance__ is usually an important key: it may be the reason why some people love documentaries and it's directly linked to the point that they compile facts and figures, and then present them in balanced perspectives to an audience that cares and has reasons to care. The more representative of true details the documentary is, based on facts, usually the better.

__Relevance__ in information conveyed is not straightforward to achieve. Ask any documentary director: it's hard, and it's often the road less travelled. So what is on the road that is overly travelled? Entertainment. Entertainment is easier to produce than balanced information perspectives, and has a major advantage, the raw promise of:

> If I can keep you entertained long enough, I can distract you from real problems. If I can keep you distracted from real problems, well, I won't need to solve them anytime soon.

And the first kicker of this post: If I'm not solving meaningful problems, or I'm generating irrelevant new ones - I'm doing __Sabotage__.

This applies for anything in life, and specifically in software projects, most of us are used to see sabotage applied on multiple distorted forms, with the [oldest tricks in the book](https://www.cia.gov/news-information/featured-story-archive/2012-featured-story-archive/simple-sabotage.html) like:
- Why we have certain "ceremonies";
- Why we throw the word "Agile" around;
- Why we haggle inefficient "carrot-in-a-stick" processes for things like career progression, promotions, paygrades, etc;
- Why we force everything through "channels" prohibiting oftentimes expedite decisions;
- Why we oftentimes are pleasant to inefficient colleagues, giving them promotions, and complain unjustly about efficient colleagues;
- Why we sometimes focus on giving praise for any thing until the act of praise itself becomes empty;
- ...

The list could go on. But out of all these things, I'd like go over in this post specifically about the ones linked to "Quality" Infotainment in its sabotage forms.

## "First, how do I spot if my project is infected with this evil?"

You might think for yourself - surely this guy is being very hardcore or harsh, I'm certain my project is free of any wrongdoing in terms of "Test/Quality/QA infotainment", or the most usual one: "this doesn't happen for us, we take careful measures to keep all the info(tainment) we produce relevant."

In these particular cases, what I try to do is invite people to actually test this out. I've done it a few times, some of them tag-teaming with close friends/testers, in what we jokingly refer to a "[come-to-Jesus moment](https://idioms.thefreedictionary.com/come-to-Jesus+moment)", not necessarily trying to make them accept my own personal faith, but providing them a fighting chance: _"a point in time in which fundamental priorities and/or beliefs are challenged, reassessed, or reaffirmed"_.

Usually by going over these examples, and comparing them to one's reality:

- Do you notice that crude/raw data counts of test cases, bugs found, bugs fixed, automated checks coverage percentages are weirdly escalated to leadership, be it first level management or close-to-board leaders, often shown as boy/girl scouts badges or participation medals?
- Do you notice that the lion's chunk of your most embarrassing bugs are often found first not by your testers, but by random folks: developers, designers, contributors of any sort, even senior leaders?
- Do you notice that your Testers are not investing the biggest chunk of their productive time doing hands-on experiential testing with sole mission of hunting down for problems and bugs that matter?
- Are your testers over-emcumbered instead with prolonged efforts of weird test documentation and automated suites maintenance?
- Do you notice any dubious decisions are made on the premise of "improving visibility of X for business/product folks", usually a target audience that doesn't really have a use for that visibility, but the decisions are still done to entertain a third party?
- Do you notice technical people using terms like: _"We need to assure our quality"_, _"We're taking these steps to improve our quality assurance"_, _"We measure quality by counting the `<insert type of bean or vegetable here>`"_, ...
- Are the technical terms above mostly proclaimed by people who, coincidenlty, are not, or never were, professional (read _craftsman_) Software Testers?
- Do you notice someone pushing for a massive pursuit of "automated check/test case" information "centralization" efforts - for a bulk of projects that to their core have no need for those?
- Are words of order reigning over facts and logic: "More Visibility!"; "Improvement!"; "Assuring!"; "Measuring Quality!";
- Initiatives are born every other week, that brew "quality/testing" documentation, some of it extensive and some of it over-simplifying, punctuated by lengthy meetings, detailed lorem-ipsum powerpoints, and cyclical meetings to follow-up other meetings.
- Do you hear the common sales-pitches: _"Our testers spend so much time on manual testing, we need more automation"_, _"Our test pipelines take hours to run, we need to revamp them and use a standard toolset"_, ... often?
- ...

How does your project score with the above? I'll give you a few moments to think.

The hard part of the above tests is that they are very hardcore depending on how you score and the current situation of your project. For some people these tests are amusing, because they understand "the catch": the underlying tone that there is undoubtely a strong and genuine focus on a particular point in some of the above tests, but that the point of focus isn't necessarily the best for the software project's context.

Other people won't find the tests so funny. They will oftentimes find them pure blasphemy, overly sarcastic, like a bad joke towards their reality. Like a self induced punch in the stomach. "We've been lied too this whole time?! I'll ignore what you're saying!". I don't blame anyone for doing just that. We've all been usually dealt a bad set of cards, here's why:

- The "default" of the industry, and the road most travelled by many of the giants (who oftentimes [don't follow what they advertise](https://www.jeremiahlee.com/posts/failed-squad-goals/)) is strongly motivated to produce content similar to all of the above tests, in line with having quality infotainment reigning over meaningul testing and actual solutions to testing (and quality) problems;
- Entertainment sells. We're encouraged make the hasty generalizations because the more "qa infotainment" content we produce, the merrier, even if it doesn't help solving problems, any assumptions and generalizations we make through the same infotainment help us appease stakeholders and distract them temporarily;
- The outliers, successful as they might be, go in direct opposition to the road most travelled, in parallel with the tech industry living and breathing for the falacy of _"appealing to authority"_: "if Google does it... if Amazon does it... if some departement in our company does it... if its an industry (or company internal) standard"... [and the beat goes on](https://www.youtube.com/watch?v=fOaxEa5ONJw);
- The falacy of sunk cost is a nasty b%$&@: "the company/project/team has initially invested so much in this road, we might as well see it throught to the end". Our heart's big desire is to get that sense of accomplishment - "We've sunk all our energy in these initiatives, we're gonna ignore any opposition, and run them to the end".

And the second kicker of this post, probably the most serious kicker I've written so far: __amusing, shocking, intolerable or offensive as the above tests might be, _the problems_ remain in almost all projects__.

From a very crude Test Strategy perspective - if in your project you're not foccusing on the hunt for embarrassing bugs, problems that matter, confusion that will bite you back, risks that will will destroy the project.... if it's not something you're investing the better portion of your energy on - any other information you might invest in producing and demonstrating, even if you don't have a fetish on it, is ultimately not helping you solve your most urgent testing problems. Testing problems require testing solutions. Testing solutions require guts, investigation, problem solving, play, nimbleness in handling relevant information, rapid adaptation to context and and a sharp situational awareness of surroundings in your project. Now compare all of the previous to any "fetish in quality infotainment" example you have in your personal life.

## So how do I get rid of this evil?

This is the part of the post where I would offer my "big brain moves" knowledge in getting rid of the evil. That might happen for an Age of Empires 2 match. But the sad reality in this case is, I don't have any. I have my own imperfect human experience I can share, and thats it.

For example, soon after starting to do these tests with some friends, where they test other people's Developer/infra/operations assumptions, while I tag-team along and do the challenge from the testing perspective, we soon started to realize we had little power to convice people, for example, folks already deep into sunk cost, that they need to have their priorities and assumptions challenged. Almost all people hate to do that.

So coming back to what I can actually share, there's at least two approaches I can think of:
1) You can ignore that the evil exists.
2) Do something about the evil existence, and cut the evil by it's root.

### First, "Ignorance is ultimate happiness"

Me and some of my friends realised, a bit too late, that no matter how much we'd try, some folks are just better off ignoring their infotainment problem. Their projects will go on. People will come and go. Old infotainment will be replaced with new infotainment. "Crusades" will be employed in the name of "Holy assurance of Quality".

Crude and raw Testing problems will remain unchanged. Sometimes hundreds of thousands in revenue will be lost overnight. Fingers will be pointed. Sources of problems will endure. And still, the projects will probably remain fairly successful, or not, because there's always bound to be some people inside that still care and still solve some problems, that have no interest or gain in indirect sabotage, who are stuck forever in battles of attrition, until they quit to embrace new (or the same) challenges.

__To be fair though:__ If the project is financially successful despite being riddled with quality infotainment, we're really not the ones to judge or to impose something else. We'd be hypocrites to do so.

Are people happy? Good! The only thing that we can do, in these cases is, if it matters, try to lead by example: show that there's another way, a better way, a harder but simpler way... and hope that that will ring a bell with someone in the organization who has a titanium forehead and a big pair of balls of steel in their desk. Here's a fictional example:

> you're in a couple of projects that you help to turn into an undeniable success, with near zero resource to quality infotainment, and a sharp direction towards meaningful testing efforts - that's something that other projects can only forcefully ignore, maybe through stubborness, which is perfectly fine and some what respectable if they're successful in their own way.

Like my dad says: _Sometimes you have to let people bang their head on the wall._

### Second, (only for the brave) you can chop off the evil by the root

The challenge with change is that change is challenging. I know... I know... bear with me. Put another way:

> "Who's gonna come and save us from ourselves when we only know one of way doing things?"

From personal experience cutting quality infotainment completely from a project is hardcore, not because it's something that might be damaging altogether (most people who know me personally know that if it dependend on me, the damage would often justify the results), but because we can't just go and do an entrance with both feet: "stop doing this" and "do this other thing instead".

Any project setup, be it a setup of meaningful testing efforts or a setup of "quality infotainment bliss" is supported by people, by ideas, by interests (both personal and project), by habit, by implicit and explicit understandings. /TODO

It's easy to hand out recipes for success if you had success in your context. I could go ahead and shout out my own words of order:

/TODO


## Wrapping up

Organized guerrilla efforts Vs. Hippy/Savage disorganization and sabotage

/TODO
