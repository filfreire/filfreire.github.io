---
layout: post
title: "On the uselessness of quality infotainment"
meta_description: "On the uselessness of quality infotainment"
date: 2020-05-13
categories: [testing, quality infotainment, love letter]
image: /assets/images/2020/05/office_space.jpg
caption: "Office Space, 1999"
---

There's an evil that found its home in a lot of software projects, be those produced in small or big tech companies, from startups to old corporations: _Quality Infotainment_.

[Infotainment](https://dictionary.cambridge.org/dictionary/english/infotainment) is _"the reporting of news and facts in an entertaining and humorous way rather than providing real information"_.

"Quality" Infotainment, from a personal standpoint, is in its core form the production and maintenance of any (irrelevant) "quality"/"QA"/Testing related information, as well as processes and efforts that are the direct opposite of meaningful testing efforts or are in fact a negative move towards solving testing problems. Typical examples comprise coming up with numbers, figures and initiatives to entertain a specific set of stakeholders in anything related to Testing, Quality Assurance and Quality Control (both of which are not Testing), while at the same time not solving deep ingrained issues with the way Testing is conducted in said stakeholders' software projects, and being often pushed in a cyclical manner, fueled by attrition and the promise that "this time things will be better, just look at these tendencies".

In my personal experience, when taken to a fetish point, meaning the effort to produce this infotainment is given blind priority over doing problem-solving that matters, is probably the most popular and simple form of sabotage of software projects from the Testing (and Quality) perspectives.

There is, I admit, value in information, and the collection and presentation of __relevant__ information. Not a day goes by without me writing some form of test reports, bug reports, automated checks, and anything similar. The emphasis being always: what problem is this solving? Does that problem matter in opposition to other problems? Am I telling the truth, or exposing facts to people whom those facts matter? __Relevance.__

And you see, __relevance__ is usually an important key: it may be the reason why some people love documentaries and it's directly linked to the point that they compile facts and figures, and then present them in balanced perspectives to an audience that cares and __has reasons to care__. The more representative of true details the documentary is, based on facts, usually the better.

__Relevance__ in information conveyed is not straightforward to achieve. Ask any documentary director: it's hard, and it's often the road less travelled. So what is on the road that is overly travelled? Entertainment. Entertainment is certainly easier to produce than balanced information perspectives, and has a major advantage, the raw promise of:

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

The list could go on... But, out of all these things, I'd like go over in this post specifically about the ones linked to "Quality" Infotainment in its sabotage forms.

## "First, how do I spot if my project is infected with this evil?"

You might think for yourself - surely this guy is not being humble or being very hardcore or harsh, I'm certain my project is free of any wrongdoing in terms of "Test/Quality/QA infotainment", or the most usual one: "this doesn't happen for us, we take careful measures to keep all the info(tainment) we produce relevant."

In any of these particular cases, what I try to do is invite people to actually test this out. I've done it a few times, some of them tag-teaming with close friends/testers, in what we jokingly refer to a "[come-to-Jesus moment](https://idioms.thefreedictionary.com/come-to-Jesus+moment)", not necessarily trying to make people accept my own personal faith, but providing them a fighting chance: _"a point in time in which fundamental priorities and/or beliefs are challenged, reassessed, or reaffirmed"_.

Usually by going over these examples, and comparing them to one's reality:

- Do you notice that crude/raw data counts of test cases, bugs found, bugs fixed, automated checks coverage percentages are weirdly and frequently escalated to leadership, be it first level management or close-to-the-board presidents, often shown in a similar fashion as boy/girl scouts badges or event participation medals?
- Do you notice that the lion's chunk of your most embarrassing bugs are often found first not by your testers, but by random folks: developers, designers, contributors of any sort, and even in some cases by senior leaders?
- Do you notice that your Testers are not investing the biggest chunk of their productive time doing hands-on experiential testing with the sole mission of hunting down for problems and bugs that matter?
- Are your testers over-emcumbered with prolonged efforts of weird test documentation and automated suites maintenance?
- Do you notice any dubious decisions are made on the premise of "improving visibility of `<XYZ>` for business ands product folks", usually a target audience that doesn't really have a use for that visibility, but the decisions are still done to entertain a third party audience?
- Do you notice technical people using terms like: _"We need to assure our quality"_, _"We're taking these steps to improve our quality assurance"_, _"We measure quality by counting the `<insert type of bean or vegetable here>`"_, ...
- Are the technical terms above mostly proclaimed by people who, coincidenlty, are not, or never were, professional (read _craftsman_) Software Testers?
- Do you notice someone pushing for a massive pursuit of "automated check/test case" information "centralization" efforts - for a bulk of projects that to their core might have no need for those?
- Are words of order reigning over facts and logic: "More Visibility!"; "Improvement!"; "Assuring!"; "Measuring Quality!"; ...
- Are Initiatives born every other week, that spawn "quality/testing" documentation, some of it extensive and some of it over-simplifying, punctuated by lengthy meetings, detailed lorem-ipsum powerpoints, and cyclical meetings to follow-up other meetings?
- Do you hear the common sales-pitches: _"Our testers spend so much time on manual testing, we need more automation"_, _"Our test pipelines take hours to run, we need to revamp them and use a standard toolset"_, ... often?
- ...

(Daily reminder there is no such thing as manual/automated testing... There's only Testing. I know... I know...)

How does your project score with the above? I'll give you a few moments to think.

The hard part of the above tests is that they are very hardcore depending on the current situation of your project. For some people these tests are amusing, because they understand "the catch": the underlying tone that there is undoubtely a strong and genuine focus on a particular point in some of the above tests, but that the point of focus isn't necessarily the best for the software project's context.

Other people won't find the tests so funny. They will oftentimes find them pure blasphemy, overly sarcastic, like a bad joke towards their own reality. Like a self induced punch in the stomach. "We've been lied to this whole time?! I'll ignore what you're saying!". I don't blame anyone for doing just that. We've all been usually dealt a bad set of cards, here's why:

- The "default" of the industry, and the road most travelled by many of the giants (who oftentimes [don't follow what they advertise](https://www.jeremiahlee.com/posts/failed-squad-goals/)) is strongly motivated to produce content similar to all of the above tests, in line with having quality infotainment reigning over meaningul testing and actual solutions to testing (and quality) problems;
- Entertainment sells. We're encouraged make hasty generalizations because the more "qa infotainment" content we produce, the merrier, even if it doesn't help solving problems since any assumptions and generalizations we make through the same infotainment help us appease stakeholders and distract them temporarily;
- The outliers of the above tests, successful as they might be, go in direct opposition to the road most travelled, like the fact the tech industry lives and breathes the falacy of _"appealing to authority"_: "if Google does it... if Amazon does it... if some departement in our company does it... if its an industry (or company internal) standard"... [and the beat goes on](https://www.youtube.com/watch?v=fOaxEa5ONJw);
- The falacy of sunk cost is a nasty b%$&@ oftentimes: "the company/project/team has initially invested so much in this road, we might as well see it through to the end". "Our heart's big desire is to get that final sense of accomplishment in rolling this stuff out". "We've sunk all our energy in these initiatives, we're gonna ignore any opposition, and run them to the end".

And the second kicker of this post, probably the most serious kicker I've written so far: __amusing, shocking, intolerable or offensive as the above tests might be, _the problems_ remain in almost all projects__.

From a very crude Test Strategy perspective - if in your project you're not foccusing on the hunt for embarrassing bugs, problems that matter, confusion that will bite you back, risks that will will destroy the project.... if it's not something you're investing the better portion of your energy on - any other information you might invest in producing and demonstrating, even if you don't have a fetish on it, is ultimately not helping you solve your most urgent testing problems. Testing problems require testing solutions. Testing solutions require guts, investigation, problem solving, play, nimbleness in handling relevant information, rapid adaptation to context and and a sharp situational awareness of the surroundings in your project.

## So how do I get rid of this evil?

This is the part of the post where I would offer my "big brain moves" knowledge in getting rid of the evil. That might happen for an [Age of Empires 2 match](https://www.youtube.com/watch?v=DBuqPjPdn0I), but, the sad reality in this case is, __I don't have any__. I have my own imperfect human experience I can share, where I need to give some space to humility, and that's it.

For example, soon after starting to do these tests with some friends, where they test other people's Developer/infra/operations assumptions, while I tag-team along and do the challenge from the testing perspective, we soon started to realize we had little power to convice people, for example, folks already deep into sunk cost, that they need to have their priorities and assumptions challenged. Almost all people naturally hate when that happens.

So coming back to what I can actually share, there's at least two approaches, based on personal experience, that I can think of:

1) You can ignore that the evil exists.

Or

2) You can do something about the evil's existence, and cut the evil by its root.

### First, "Ignorance is ultimate happiness"

Me and some of my friends realised, a bit too late, that no matter how much we'd try, some folks are just better off ignoring their own infotainment problem. Their projects will go on. People will come and go. Old infotainment will be replaced with new infotainment. "Crusades" will be employed in the name of "Holy assurance of Quality".

Crude and raw Testing problems will remain unchanged. Sometimes hundreds of thousands in revenue will be lost overnight. Fingers will be pointed. Sources of problems will endure. And still, the projects will probably remain fairly successful, or not. The hope in those cases is that there's always bound to be some people or teams inside that still care and still solve some problems, that have no interest or gain in indirect sabotage, who are stuck forever in battles of attrition, until they quit to embrace new (or the same) challenges.

__To be fair though:__ If the project is financially successful despite being riddled with quality infotainment, we're really not the ones to judge or to impose something else. We'd be hypocrites to do so.

Are people happy? Good! The only thing that we can do, in these cases is, provided it matters, try to lead by example: show that there's another way, a better way, a simpler way... and hope that that will ring a bell with someone in the organization who has a titanium forehead and a big pair of balls of steel in their desk. Here's a fictional example:

> you're in a couple of projects that you help to turn into an undeniable success, from a project standpoint and even maybe from a revenue point, with near zero resource to quality infotainment, and a sharp direction towards meaningful testing efforts - that's something that other projects can only try to forcefully ignore, maybe through stubborness, which is perfectly fine and somewhat respectable if they're successful in their own way.

Like my dad says: _Sometimes you have to let people bang their head on the wall._

### Second, (only for the brave) you can chop off the evil by the root

The challenge with change is that change is challenging. I know... I know... bear with me. Put another way:

> "Who's gonna come and save us from ourselves when we only know one of way doing things?"

From personal experience cutting quality infotainment completely from a project is hardcore, not because it's something that might be damaging altogether (most people who know me personally know that if it dependend on me, the damage would often justify the results), but because we can't just go and do an entrance with both feet: "stop doing this" and "do this other thing instead".

Any project setup, be it a setup of meaningful testing efforts or a setup of "quality infotainment bliss" is supported by people, by ideas, by interests (both personal and project), by habit and by implicit and explicit understandings.
All of these parts that support the setup create constraints that allow for an easier (or harder) chance of getting rid of quality infotainment. My first inclination is to jump forward and start shouting, with no humility whatsoever. But it's a bad attitude altogether: Being used to fail fast doesn't mean you can translate yourself well in contexts averse to failing fast. So for most people it would apparently be easy to hand out "recipes for success" and I could go ahead and shout out my own words of order:

- "Forget about counting all those beans (test case counts, bug counts, coverage counts, ...)!"
- "Stop trying to enforce the same box in diverse development and project contexts!"
- "Start investing more in experiential hands-on testing!"
- "There's a reason why your vice presidents keep finding embarassic bugs that you're missing!"
- "Perform tests that matter!"
- ...

The thing is, the problem is complex, and all of the above "words of order" don't necessarily compute on the other side. We have to take into account the "target system" and its dynamics. Think of a team that produces quality infotainment "for a living". There's so many underlying dependencies and barriers, known and unknown, with regards to sustaining the production of infotainment, that just arrogantly shouting words of order won't do the trick:

- There's __Education barriers__: Stakeholders might be finding embarassing bugs first, but translating to them that the fact they do so because "maybe we're not doing good testing ourselves" is a hard flag to raise up - first, because not a lot of people are educated in Testing (and likewise in Quality Assurance and Quality Control); Second because it's easier to entertain and prolong sinking costs into current "distractions" towards that lack of education, than to admit that theres a problem both in everyone's shared understanding of what Testing is, as well as admiting that after reaching that understanding, it turns out all along we weren't doing good testing;
- There's even __More education barriers__: It might be the case that people that comprise the team really don't know any other way. Add to that the whole attrition of having to put out fires and maintain an "infotainment machine" - there's little slack for education in testing.
- There's __communication barriers__ directly linked to the organization's design - in some teams it might be easier to shift into good testing, because testing problems can be handled in expedite direct communication, where as other teams are encumbered (and miserable) with maintaining "bullsh#$" channels with people who don't understand (nor want to understand) testing problems.
- And finally, among many other barriers, likely the biggest of all: __"Expectation management" barriers__. Linked with both communication and education barriers, these grow out of different forces happening in the system at the same time. A simple example: person A expects person B to produce bug counts for some dumb reason, because person A thinks person C will value having that information. Person C learns to expect that information, not knowing it's futile or useless information. And this grows and is prolonged in the organizational structure because there's no straightforward shared understanding on the futility of certain expectations. So in the end you can gather a crowd around managing expectations that really don't support or solve any testing problems, all born out of managing wrong expectations from the start.

All of the above barriers and many more prevent the straight cut of "the root of all evil", aka the futile production of Testing and quality information that only serves to entertain. So we've hit at this point another wall. What really can we do?

Well, if there's one thing I'm learning through time is that the simplest of ways to overcome these barriers, as opposed to shouting words of order or entering into arguments, is deep dive into straightforward principles and "self-analysis" questions, following them in a context-adapted way:

1) Whatever the project might be - as a Tester I understand and uphold that there is no such thing as "assuring quality". It's not my job to assure quality. It's not my job to advertise or promote that wrong teaching. My job and main mission is to hunt down bugs, problems and risks that matter, using my brain, tools and code, all three of them interchangeable.

2) If we're not finding embarassing and important bugs - we're probably not testing well.

3) If we're not testing well - we need to check which contraints are preventing us from doing good testing.

4) If someone else is finding our embarassing and important bugs first - they're closer to the truth than we are.

5) We don't improve at overcoming testing problems by doubling down on paths that led us away from doing good testing in the previous iteration.

6) Are our sources of advice and guidance spotless? Meaning, do we follow folks and teachings based on actual endeavors to build, run, test and maintain systems in production, in a self sufficient manner... or we pursue folks, blog posts, trends, etc, who conduct and/or sell scientific experiments and embellished "modes de vie"?

7) Ask ourselves if the testing (or quality) problem(s) we're trying to solve is(are) meaningful, or it(they) exist(s) as an excuse for a solution to stand/be pursued?

8) If we depend on crutches to do our testing efforts - chances are we'll stay dependent on crutches, and these will remain through time, even if in multiple different iterations. And crutches here can mean anything: past decisions, enforced standards and rule-sets that don't apply to context, strict or enforced pathways that don't deal with reality...

9) Visibility, and promises of its increase are as fake as ads to increase genitalia: You and your project companions either have your eyes open (or closed) towards problems that matter.

There's more principles, but these are the ones I prefer to use to keep quality infotainment at a safe distance.

## Wrapping up

A lot of words to express my ultimate feeling and belief: In the Software Testing craft, relevance in information, processes, decisions, and approaches towards testing problems ís an invaluable treasure that should be cherished and nurtured, and is in most cases incompatible with a vain illusion of control of quality information.

To fight for relevance when solving testing problems in an industry that often is more directed to prolonging and upholding futile "quality entertainment", oftentimes paying lip service to Testing, is a complex problem with a non straightforward solution.

Finally, I think there's always hope. There's a better way for the industry to do good Testing, possibly by sharing some of the principles I proposed above, but it can only happen if we stop investing in a "generalised reassuring/feel-good/measure quality" mindset, and we recognize it for what it actually is: a frivoulous attempt at feeling "safe" in software projects - in an environment where more and more we need as Testers to be the flagcarriers of the opposite: we cannot deceive ourselves now with all the quality infotainment humanely possible to produce, or else we're setting ourselves up for some really nasty and embarassing bugs directly affecting those we claim to represent, protect and obsess about: our users.

Thank you for reading. Feel free to reach out to me with comments, ideas, grammar errors and suggestions via any of my social media. Until next time, take care!