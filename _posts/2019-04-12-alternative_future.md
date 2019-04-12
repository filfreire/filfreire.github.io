---
layout: post
title: "An alternative testing universe"
meta_description: "An alternative testing universe"
date: 2019-04-12
categories: [testing, xdsd, future]
image: /assets/images/2019/04/poirot.jpg
caption: "Agatha Christie's Poirot TV Series, 1989—2013"
---

If you've read my [dystopian testing future post](https://filfreire.com/posts/dystopian_future), you might have caught up with one of my points of view of the industry, more specifically - "testing sweatshops".

Now, I believe there's another thing that's appearing in the horizon, besides "testing-as-a-service" vendors and sweatshops that needs to be mentioned, say, before "good or bad things happen".

A few years ago a known (and a bit controversial) programmer, [Yegor Bugayenko](https://yegor256.com), started paving the blocks for his own development methodology that, in his words:

> aims to reduce risks and improve quality in a project of almost any size.

The methodology I'm referring to is [Extremely Distributed Software Development](https://www.xdsd.org/XDSD-WhitePaper.pdf). The sort of "too long didn't read" explanation of the methodology is something like:

> picture a documentation-first software project, with hardcore strict code quality, hardcore strict development-process, every deliverable is specified in a small way, programmers and testers are paid only after releasing those deliverables, there are no human managers, there's almost zero human-human interaction outside of the code repository and ticketing system, no salaries, bugs are non-blocking of releases, every deliverable is so small and unique that any programmer of a pool of skilled programmers may code and deliver it to production in no more than a few hours and get paid for it in a matter of minutes, ...

My description of it, of course, falls short of the original descriptions, but from looking quickly at it, and reading diagonally, it's a bit of a weird methodology. Some people think it's beautiful and practical, efficient. Some people think it's scary, utopian, and almost all people I've talked with in person about it think it's a crazy methodology for mad people.

Whatever is one's take on it: It's happening right now.

Its inception shouldn't go unnoticed to testers. [Yegor](https://yegor256.com) founded a company called [Zerocracy](https://www.zerocracy.com/) with the major purpose of putting this methodology into practice, providing it as a service, and acting as a marketplace where developers and projects can meet. If it does end up succeeding as a methodology and a business and spreads and grows bigger in the industry, for sure, whether one sees it as a good or a bad thing: it will have an impact in the testing craft.

## Experimenting with Zerocracy

In order to go over the impacts of it for testers, I decided to try it for myself.

I must have been one of the first people to try out Zerocracy and its bot, [0crat](https://www.0crat.com/) quite some months ago after its launch. Starting to work "inside it" can be daunting for anyone: you have, similarly to the approach envisioned for projects hosted within Zerocracy, to deal first with its documentation, [the policy](https://www.zerocracy.com/policy.html), and from the start it's designed to require as little human contact as possible: "supposedly", everything should be explained in the documentation, if it's not, people are encouraged to create tickets for other people to solve and add the missing documentation or answer seemingly unknown questions.

Registration felt a bit cumbersome since it involved multiple separate steps: identify yourself as a "real person"; select one of many available projects; define a rate of how much you want to earn per deliverable; define a wallet to receive payments.

After registration, I picked a project that had 0 funds (meaning it's a regular opensource project, and you don't earn any money whatsoever), and started working on tickets and reporting bugs I found along the way. On a personal level, I noticed two interesting things while working:

- from a developer standpoint I felt motivated to contribute more to the opensource projects linked to the platform because each contribution felt small, sort-of brain-teaser like, and at the same time crucial. Sometimes the troubles came from the fact I had to wrap my head around the idea of making small changes and then trying to have them merged, and I either made meaningless changes or too-big changes to be quickly reviewed, improved and merged.

- from a tester standpoint - reporting bugs felt right, in the sense that I had to make sure they were meaningful, and it felt like a clutter-less experience: found a problem, be it big or small, report it, get the score, repeat. The mindset it usually placed me under felt appropriate: I'm investigating and hunting for issues at my own pace, and I don't need to abide by some obtuse corporate structure that sometimes hinders deep testing (example: "We can't release something into production unless testers test"). The testing efforts felt independent and supercharged.

There's more to be said about my personal usage of Zerocracy (ZC), but for the purposes of what I wish to discuss in this post, I'll stick for now to what I mentioned above.

I'd say the experience overall feels unnatural to what one experiences in a corporate/office environment in most software projects, even though I had it easier than a lot of people who hadn't previously read about or were unfamiliar to XDSD or to Yegor's ideas, I still had difficulties. Also noteworthy, for a long time, it seemed like there was always this stream of newcomers who always took the "lazy" path and asked people in the ZC telegram chat questions that were in the documentation.

Let's now go over some initial observations I have, after experimenting with ZC platform and model, from a testers-view point.

## Issues in ZC that impact testing craft

There are __four__ main points about ZC that I believe will impact testers. The first point, to me, the biggest concerning point that ZC model impacts the testing craft, and I'll spend some more time discussing it:

### 1) Paying for bugs - a double-edged sword

 In the ZC model, it's ultimately not about paying a person for sitting around and doing something, it's always about deliverables, and in the case of Testers, the main deliverable, and the sole plainly advertised one is Bugs. In this and before going forward, I think it's important to take into account, context-wise, what is considered a bug in the ZC Model:

> A software bug is an error, flaw, failure, or fault in a computer program or system that causes it to violate at least one of its functional or non-functional requirements. ([source](https://www.yegor256.com/2015/06/11/wikipedia-bug-definition.html))

My idea is: motivating bug "hunting" primarily with money is a curse if what you're looking for is skillful testing. If I'm only focused in making money, I won't waste time in sharpening my skills if I have instant money gratification.

From experience, I'd say I find more meaningful bugs for any given project when my main focus and motivation is to "just" test: to investigate, to hunt down, to research, to learn, to play. On the opposite side and also from personal experience: When I'm not motivated by sheer will and an act of, say, learning or play: I find I'm more prone to find less important bugs for any given project.

To put it in analogy: Say you want to uncover something really secret, and you pick from a pool of a number of private detectives, whom you might entice using money per findings for a good number of good detectives - but what of [Hercule Poirot](https://en.wikipedia.org/wiki/Hercule_Poirot), the best detective of all? For such a creature - money is secondary, and entertaining his "little gray-cells" is his true "life-force".

There are two sides to any coin: there are moments it definitely feels more enticing to get paid for bugs, than to get paid a salary to be a hollow-cheerleader, to tell lies and sit in the office pretending you're testing, only for the product manager to use you as a green-light and a "gatekeeper" of bugs, and to ask you: "are we good for a release?", and later on, blame you for bugs not found in production. If I had to choose only one, the first option seems better for any tester that loves their craft.

Working in small chunks and getting paid for chunks delivered, might be wonderful for developers pushing out code faster, but for testers its a possible handicap on the projects, where I think each of the projects will start seeing in time a pattern where only certain kind of both important and both superficial bugs are being reported. If the project can live with this, sure that's fine, but I don't think most projects do. And in this sense greediness does not benefit the tester's role in the same way ZC believes it benefits programmers. Testers are a tremendously important and unique support branch of projects, and you wouldn't want someone supporting your project to be a greedy animal and omega mercenary, in the same sense you wouldn't want a nurse or a radiologist at a hospital to be greedy, it wouldn't work well for the patient.

It's a slippery road, I admit there's also other ideas to consider:

- Maybe bugs should have different labels - is it a meaningful bug? is it a superficial bug? Is it a crappy bug (should one still get paid for a badly reported bug, or given a special chance to improve it?) ?
- The amount paid for that bug needs to take into account both the labels (maybe they can be priced as extras given to the tester) and also the testers rate.
- Maybe the rates for the different bugs can also be programmed in a sort of a seasonal way, that you get paid more (or less), depending on the stakeholders preference, to find bugs in different seasons, say, before the stakeholder decides to do a release, based on the stats of how many meaningful bugs have been reported throughout time.


### 2) Confusion and questions

Yet another point of discussion with viewing bugs as the main and sole deliverable of Testers within the ZC model is, and expert testers know this: A lot of times a survey session, or even a deep test session might not result in bugs that are critical. How do we reward a tester who might have produced a good test session report but ultimately hasn't found noteworthy bugs? Maybe only found some questions or some confusion. What do we do in that case? Do we pay the tester for the session report? Do we pay the tester for ticketing the questions and ticketing the confusion? What would "ticketing the confusion" look like and would the project reward the tester the same way? To me, this is still unclear in a practical level, even if it's advertised or mentioned/marketed, and it's a key component of testing that is missing out or not really apparent in ZC.

Sure enough, the counter-argument can be: "Oh, but indeed we recommend people to raise tickets and questions". In all honesty, I've seen my fair share of opened tickets with questions and confusion that remain open for quite a long time (to avoid saying "forever"). I've also seen people giving up, and not even bothering to create a ticket after getting a bland reply to "create a ticket".

I'd say there's still no real underlying motivation in reporting these specific types of issues of confusion/questions - especially since it's time that is being "diverted" of the reporters that the project is not actively paying/rewarding for, but is a crucial time for example for testers. There's also no effective registry for the questions and confusion that are happening in other comunication channels outside of Github (Example. Telegram channels) - that end up being a repeated pattern of problems that seem to never get properly reported and fixed because it always feels like its not rewarding to report them or fix them.

The fact that people keep asking questions and voicing confusion via alternate comunication channels and other people keep replying "create a ticket for it" seems like a bug to me, that has gone unreported since the inception of Zerocracy: there's to this date, no active and apparent and practical, for dummies, reward in trying to tackle and voicing questions in the ticketing systems - at least not while one still sees people asking the same questions every day regarding a system that supposedly wouldn't be dependent on human-human interaction, to begin with.


### 3) Junior Testers

The role of an inexperienced/junior tester is also unclear. Possibly the quality of the bugs reported won't be good. In this I think the role envisioned for the QA (different from the role of a tester), or even for a senior tester within the ZC model might help both minimize this while getting the extra testing efforts from juniors: the QA in the team and the more Senior Tester can both review and get paid for reviewing the junior tester bug; the senior tester might also get paid for plainly improving that bug. I'm not sure about this, but definitely is a topic that requires some thought.


### 4) Communication

For me as a developing-craftsman tester, there's another big hole in ZC and XDSD as a model in this point: What about communication in testing?

A crucial part of being a tester, similarly to an investigator, is the human-human interaction that in ZC by design shouldn't exist.

> Excellent testing requires testers to have some degree of technical skill, but also to have the social skills, the communication skills, and the domain knowledge to test effectively. ([source](https://www.developsense.com/blog/2018/12/who-needs-the-testers/))

Working with ZC model doesn't necessarily mean testers don't need social skills or communication skills (written at least), but barring almost all communication is, I believe, yet another problem that needs review and thought:
Testers, in order to perform testing efforts are required to hunt for information, and especially specification anywhere, be it documentation, the product itself, email threads, chat logs, logs, other bugs reported, and as important as the channels mentioned above, talking with testers, developers and client representants, asking questions to other humans. By cutting the human-human interaction, we might be dumbing down a key part of Skilled testers that is interpersonal communication.

Sure, one might say: but the "acquiring" of information through any means in this case changes, you lose some channels of communication, but you get credited and paid for reporting tickets with questions, with information requests, with doubts and problems and confusion. Yeah sure, but there are observations that a tester can only make when in contact with other people. We must not forget that the main advantage of the tester is we're talking about someone specialized and skilled in "learning about your product" first (not to be mistaken with learning about testing). Blocking human interaction within the project may be considered a switch for decreased learning. I also understand this: sure, in the digital age, maybe you can minimize this with recorded videos, and some kind of VoIP calls. Maybe. But it still seems like a topic that requires thought, because currently as it is, it seems overlooked.

These are some of the initial points I have on the platform, time and more experimenting will tell me if there are more problems or benefits with the ZC model.

## Wrapping up

Presumably, by reading the [testimonials](https://www.zerocracy.com/testimonials.html) page, it's signaled that there are already some people with money and projects and businesses that are picking up on it, and using it. And guessing by the positive testimonials some of them notice the four advertised things on [Zerocracy](https://www.zerocracy.com/)'s webpage:

- Reduced labor costs;
- Not having to deal with personnel turnover;
- High maintainability of the projects, because of the communication restrictions;
- High quality of code, because of the code-quality and development restrictions;


I don't know about the negative testimonials, and at the rate that a lot of posts and videos are made with explanation after explanation of the inner workings of the ZC service and the methodology, I infer that [Yegor](https://yegor256.com) understands that it'll probably take some time for this whole deal to make a lasting impression in the industry.

Truth is I don't know, I'm not the one to say whether this is a good business model or not. I'm also not one to make judgments of the methodology, I won't digress in this post with whether or not I think it works or it's just all a crazy business. But I underline what I've said before: this model is already into action, it's possible and probable that more and more business owners will pick up on this model, buy it for its views on "pay-what-you-get" developments, and testers need to be on the lookout for this, and [Yegor](https://yegor256.com) and the people over at ZC should invest time thinking on a better meaningful structure for testers within Zerocracy. Maybe the concept of [Raid-ST](https://raid-software-testing.com/) can be for example adapted to ZC, and we motivate expert testers both on finding and reporting bugs, as well as solving other quality and testing issues in projects. I don't know yet, but it's definitely food for thought for the future.
