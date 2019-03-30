---
layout: post
title: "An alternative testing universe"
meta_description: "An alternative testing universe"
date: 2019-02-29
categories: [draft]
image: /assets/images/jp_404.jpg
caption: "Replace this, 2018"
---

> Disclaimer:

If you've read my [distopian testing future post](TODO), you could observe a short summary of my probably flawed/biased point of view of the industry.

But, I believe there's another thing that's appearing in the horizon, besides "testing-as-a-service" vendors and sweatshops that I'd like to talk about, and something that I think needs to be raised and discussed, say, before "good or bad things happen". Keep in mind the "labour resource" notion mentioned before.

A few years ago a known (and a bit controversial) programmer, [Yegor](https://yegor256.com), started paving the blocks for a development methodology that, in his words:

> aims to reduce risks and improve quality in a project of almost any size.

The methodology I'm referring to is [Extremely Distributed Software Development](https://www.xdsd.org/XDSD-WhitePaper.pdf). The sort of "to long didn't read" explanation of the methodology is something like:

> picture a documentation-first software project, with hardcore strict code quality, hardcore strict development process rules, every deliverable is specified in a small way, there are no human managers, there almost zero human-human interaction outside of the code repository and ticketing system, no salaries, bugs and defects are non-blocking of releases, every deliverable is so small and unique that any one programmer of a pool of skilled programmers may code and deliver it to production in no more than a few hours and get paid for it in a matter of minutes, ...

My description of it of course falls short of the original descriptions, but from the looks of it, it's a weird methodology right? Beatiful? Scary? Utopian? Crazy? You can read more about it in the link. But for the purposes of this post, I want to focus on why it matters for testers.

Whatever is one's take on it: It's happening right now.

It's inception shouldn't go unnoticed to testers. [Yegor](https://yegor256.com) founded a company called [Zerocracy](TODO) with the major purpose of putting this methodology into practice, providing it as a service. If it does end up succeding as a methodology and a business and spreads and grows bigger in the industry, for sure, whether one see's it as a good or a bad thing: it will have an impact in the testing craft.

I decided to try for myself, and look a bit into the possible impact it may have on the testing craft.

## Experimenting with Zerocracy

Here's what I did...
/TODO

## Initial observations

Let's now go over some initial observations I have, after experimenting with ZC platform and model, from a testers-view point.

In the ZC model it's ultimately not about pay a person for sitting around and doing something, it's always about deliverables, and in the case of Testers, the main deliverable, and the sole plainly advertised one is Bugs/Defects.  In this and before going forward, I think it's important to take into account, context-wise, what is considered a bug in the ZC Model:

> a bug is (...) [yegors post about bugs](TODO)

Getting paid for bugs can be both a good thing and a bad thing. In my experiments for example, on one hand I did indeed feel motivated to find more bugs. There was this joyful feeling of getting paid and an almost instant reward, and recognition in the form of money for bugs that I took care in reporting, and tried to report as well and with a meaningful description as I would. But this joy can be so brittle/short and it may very well lead me to a path that is not a craftsman path. If I don't control my motivations, I start less and less motivating by researches with plain love for finding things out and plain love for testing, and replace that with money, it might be a motivation that ultimately dulls my senses: "I'm only foccused in making money, I wont waste time in sharpening my skills if I have instant money gratification". This whole instant gratification deal might be personal to me, and other testers wouldn't feel this, and would have no problems in staying sharp, but I know that as a human it's a slippery slope when the main motivation is money.

I don't have a problem with getting paid, it's way much better to get paid for bugs, than to get paid a salary to be a cheerleader, to tell lies and sit in the office pretending you're testing, only for the product manager to use you as a green-light and a "gatekeeper" of bugs, and to ask you: "are we good for a release?", and later on blame you for bugs not found in production. If I had to choose one, the first option seems better for any tester that loves their craft.

Added to this let's not forget that the main motivation behind this is the "work with greed" not with "fear of management".

Again, my problem is losing sharpness. The greedyness part of ZC might be wonderful for developers pushing out code faster, but for testers its a possible handicap on the projects, where each of the projects will start seeing in time a pattern where only certain kind of both important and both superficial bugs are being reported. If the project can live with this, sure that's fine, but I don't think most do. And in this sense greedyness does not benefit the testers role in the same wait ZC believes it benefits programmers. Testers are an tremendously important and unique support branch of projects, and you wouldn't want someone supporting your project to be a greedy animal and omega mercenary, in the same sense you wouldn't want a nurse or a radiologist at a hospital to be greedy, it wouldn't work well for the patient.


Regarding the "getting paid for bugs" I think theres also other things to consider:
- Maybe bugs should have different labels - is it a meaningful bug? is it a superficial bug? Is it a crappy bug (should one still get paid for a badly reported bug, or given a special chance to improve it?) ?
- The ammount paid for that bug needs to take into account the both the labels (maybe they can be priced as extras given to the tester) and also the testers rate.
- Maybe the rates for the different bugs can also be programmed in a sort of a seasonal way, that you get paid more (or less), depending on the stakeholders preference, to find bugs in different seasons, say, before the stakeholder decides to do a release, based on the stats of how many meaningful bugs have been reported throughout time.


Yet another point of discussion with viewing bugs as the main and sole deliverable of Testers within the ZC model is, and expert testers know this: A lot of times a survey session, or even a deep test session might not result in bugs that are critical. How do we reward a tester who might have produced a good test session report but ultimately hasn't found noteworthy bugs? Maybe only found some questions or some confusion. What do we do in that case? Do we pay the tester for the session report? Do we pay the tester for ticketing the questions and confusion? To me this is unclear, and it's a key component of testing that is missing out or not really apparent in ZC.


The role of an inexperienced/junior tester is also unclear. Possibly the quality of the bugs reported won't be good. In this I think the role envisioned for the QA, or even for a senior tester within the ZC model might help both minimize this while getting the extra testing efforts from juniors: the QA in the team and the more Senior Tester can review and get paid for reviewing the junior tester bug; the senior tester might also get paid for plainly improving that bug. I'm not about this, but definitely is a topic that requires some thought.


For me as a developing-craftsman tester, there's a big hole in ZC and XDSD as a model in this point:

What about communication in testing?

A crucial part of being a tester, similarly to an investigator, is the human-human interaction that in ZC by design shouldn't exist. Communication as a main topic is fairly reported in all the most important testing advocates and experts contents, [example 1](TODO); [example 2](TODO); [example 3](TODO)

I think this a serious problem that needs review and thought:
Testers, in order to perform testing efforts are required to [hunt for information, and specially specification](TODO) anywhere, be it documentation, the product itself, email threads, chat logs, logs, other bugs reported, and as important as the channels mentioned above, talking with testers, developers and client representants, asking questions to other humans. By cutting the human-human interaction, we might be dumbing down a key part of Skilled testers that is interpersonal communication.

Sure, one might say: but the "acquiring" of information through any means in this case changes, you lose some channels of communication, but you get credited and paid for reporting tickets with questions, with information requests, with doubts and problems and confusion. Yeah sure, but there are observations that a tester can only make when in contact with other people. We must not forget that the main advantange of the tester is we're talking about someone speciallized and skilled in "learning about your product" first (not to be mistaken with learning about testing). And blocking human interaction within the project may be considered a switch for decreased learning. I also undestand this: sure, in the digital age, maybe you can minimize this with recorded videos, and some kind of voip calls. Maybe. But it still seems as a topic that requires thought, because currently as it is, seems daunting/bad?


These are some of the initial thoughts I have on the platform, time and more experimenting will tell me if there are more problems or benefits with the ZC model.


## Wrapping up

Presumably, by reading the testimonials page, it's signaled that there are already some people with money and projects and businesses that are picking up on it, and using it. And guess by the positive testimonials some of them notice the four advertised things on [Zerocracy]()'s webpage:

- Reduced labor costs;
- Not having to deal with personnel turnover;
- High maintainability of the projects, because of the communication restrictions;
- High quality of code, because of the code-quality and development restrictions;


I don't know about the negative testimonials, and at the rate that lot of posts and videos are made with explanation after explanation of the inner workings of the service and the methodology, I infer that [Yegor](https://yegor256.com) understands that it'll probably take some time for this whole deal to make a lasting impression in the industry.

Truth is I don't know, I'm not the one to say whether this is a good business model or not. I'm also not one to make judgements of the methodology, I won't digress in this post with whether or not I think it works or it's just all a crazy business. But I underline what I've said before: this model is already into action, its possible and probable that more and more business owners will pick up on this model, buy it for it's views on "pay-what-you-get" developments, and testers need to be on the lookout for this, and [Yegor](https://yegor256.com) and the people over at ZC should really invest more time thinking on a meaningful structure for testers within Zerocracy. Maybe the concept of [Raid-ST](TODO) can be for example adapted to ZC, and we motivate expert testers both on the front of finding and reporting bugs, as well as solving other quality and testing issues in projects. I don't know yet, but it's definitely food for thought for the future.
