---
layout: post
title: "Why Opensource projects fail?"
date: 2019-01-21
categories: [opensource, development, quality]
image: /assets/images/2019/01/jp3.jpg
caption: "Jurassic Park 3, 2001"
---

> **Disclaimer**: this is a personal account based on my observations as a regular OSS contributor. Experience and observations will certainly vary from person to person.

Recently I've done an [internal session](/talks) at Adidas about the pros of following practices of some of the best opensource projects in a corporate environment, and how those deeply impact both the quality of the development process and also in some ways the perceived quality by the end-users of the developed product.

In a summarized way, the points I mention in the talk are pretty much "no-brainers" for people who contribute or follow regularly to opensource projects:

- Typically companies have a hidden (or visible) "ship fast or die mindset";
- Some companies defend some nasty concepts, with the excuse there is guaranteed success when (only) follow footsteps of giants (like Spotify, AWS, etc.);
- We fail to see that "opensource" "is all around us, it bind us" (like the Force in SW);
- We need the same rigour & code quality we see in the best OSS projects;
- We need to focus on 1 meaningful and important problem at a time;
- We need to aim for Sustainability and Maintainability (being agile does not mean being blazing fast and a good slave);
- "No time to test" is a myth;
- "No time to document" is a myth;
- Bug reports shouldn't be "apply template here" - they should be meaningful;
- Testing in OSS is not "counting test cases or covering everything with a reactive nonmetal based checking library";
- OSS projects self-evaluate;
- Lessons of Motivation, happiness, and drama in OSS - these are way bigger than in the corporate world;


The basic idea to wrap up that talk was that OSS projects live, survive and adapt longer: a lot because of quality; Also, the OSS development described "slowness" by non-coding people and the picture that its development model is unfit to the corporate world is also a myth, and we can change a bit in our work every day.

At one point a dear colleague of mine mentioned that it would be interesting to see the reverse of the coin: why do some OSS projects fail, fall into abandonment, and how some of them manage to survive an impending failure to this day. I think these points are as important to go through as are the more "positive, we can change the corporate" world points, so what follows in this post is a collection of observations I've made over time to directly touch these topics of the "failure" side of things.

## Emotional motivation for abandonment

I believe that one reason projects get abandoned or fail is because of "life" and not necessarily because the maintainer is a crappy or evil human. It's most times because of the reasons you'll find maintainers typically writing about. The life of a maintainer is not an easy path. For example, here's [an interesting read](https://nolanlawson.com/2017/03/05/what-it-feels-like-to-be-an-open-source-maintainer/) that goes over what it feels like to be a maintainer.

Tinkering and coming up with a piece of code and putting it online for the world to see is one thing. Making it maintainable is another thing. Maintaining it over a prolonged period of time is yet another thing. OSS is hard-work sometimes for simple reasons: life, for better or worst, gets in the way and finds a different way ([Jurassic Park pun unintended](https://www.rottentomatoes.com/m/jurassic_park/quotes/)).

- You come home tired from work;
- You want to spend time with your family;
- You want to spend time with your other hobbies besides programming;
- You want to go outside and do something;
- You can't see another computer in front of you after hours of tackling with one at work;
- ...

All of these are normal. I personally believe we should never bash people who stop maintaining stuff for any personal reason whatsoever. Life is hard for everyone. If for any reason you think the maintainer is not being responsible, don't bash the maintainer, go the other way, fork the project, start your own branches with your ideas and improvements, direct other people towards your branch, and do things in a way that you're still appreciating someone else's initial work.

(Note: There's also an interesting take on this, discussible to an extent, that some of the excuses for not contributing to OSS, detailed for example in [this post](https://www.yegor256.com/2015/12/22/why-dont-you-contribute-to-open-source.html) are somewhat poor excuses looking from a certain angle. Food for thought: could it be that for instance, maybe, at one point maintainers stop caring? If one does not contribute, does it really mean one does not care?)

## Set for abandonment

**The documentation is ~~garbage~~~ non-existent** - on a personal level this is the worst indicator for me. It tells me the project is from the start not set for maintainability. It's a bit of a dirty hobby, but I do this over time: when I see a project doesn't have a readme, or the readme clearly misses to say how I can build and use the project on my local machine, I open an issue exactly to tackle that. This is not an isolated problem, it happens in the most diverse projects.

**Documentation is there, but to build on your machine you need sorcery, and tackle build errors that "StackOverflow will only have an answer in 2-3 years"**. ([XKCD comic #979 is a good example of the feeling](https://xkcd.com/979/)) The next logical step after documenting it is: make it run in a CI solution. There are countlessly available, from [Travis](https://travis-ci.org/) to [CircleCI](https://circleci.com/), free for opensource projects, and yet, sometimes people just avoid these, in their minds "oh I don't need this, I can build fine on my own machine". The thing is your machine is not my machine or the person's next door machine. The easiest way to guarantee that the person next door will have a good chance of building your project locally is plainly making it build on CI. It's confusing, and maybe for some people it'll take 5 minutes for other people 5 days, but the benefits are there once it's set up: chances are better for potential contributors to be able to build your project locally or by setting it to build on CI you'll run into blocking points that a future contributor will run.

**The last commit was pushed "in 1942, before going on a covert-ops mission in North Africa"**. This point is a no brainer. If the project hasn't been updated for years if the CI seems abandoned, if there are tons of issues or pull-requests open and not a single reply from the maintainer.

## Set for survival

**Replying soon, reviewing soon, merging soon**. Recently a colleague of mine, [@jmromanos](https://github.com/jmromanos), opened an interesting PR in [danger](https://github.com/danger/danger/pull/1047) repo. In a matter of minutes, the PR was reviewed, merged, and my colleague invited to be a maintainer, with the premise of this [policy](https://github.com/danger/danger/pull/1047#issuecomment-445808144);

This is the best recent example I found, where in a matter of minutes, a few days work of a PR was quickly reviewed, acted upon, and in this case, since the code review was accepted, there was an outright attempt of follow-up with the contributor to "join the ranks" of other maintainers.

Another example hit close to home recently with [Sara Vieira](https://twitter.com/NikkitaFTW)'s recent [pull-request in Tacit CSS](https://github.com/yegor256/tacit/pull/173). The fix was simple, the change was small, and the benefits of merging were an outright win, so I used [Rultor](http://rultor.com) to quickly merge and tag a new release so anyone could use the newer version of [Tacit](https://github.com/yegor256/tacit/pull/173#issuecomment-449992742) with the fix.

A lot of times this sort of "quick-action/quick-follow-up isn't possible for many different reasons. Maybe the pull request leaves open-ended questions. Maybe it's not right the first time after code review, and then it slows down the chances of it getting merged any time soon. A lot of "maybes", all of them causing the project to be less appealing for newcomers. The faster we can try to react to a PR on an issue, the better chances the same person will contribute again or attract more contributors, and the project won't get easily abandoned.


**Pay contributors in money, not in exposure**: Some of the projects I've contributed towards for example are set in a way that you can pay contributors to help you fix or develop issues that affect you. I think this is fine. There are a couple of strategies for this:

- from a "no-human-manager" and projects are financed in a way anyone can contribute and be monetary rewarded, an approach you'll find in contexts like [zerocracy](https://zerocracy.com);
- to a "pay for an expert and active contributor of a project for a tailor-made adaptation of the project, as you'll find in some funded OSS projects like [geonetwork](https://www.geonetwork-opensource.org/). At one point in my life I had to use it and I soon found out that a few of the main maintainers were also doing something very bright: if you as a user of that OS project wanted a specific new feature or some sort of support beyond the normal documentation of the project, you could easily reach out one of the maintainers and hire "consultancy" work from them.

This last approach,

> the software is "free" as in "free beer" and its code is almost entirely open, but you pay contributors for support

is not entirely new, a lot of folks from the Linux-"Universe" ([example](https://www.redhat.com/en)) have been doing on a lot of fronts something similar for quite some time, but the bottom line is: if you want more from what we're doing out of love and our personal passions, you better pay for it.

> **Advice**: Beware of [Choosing beggars](https://www.reddit.com/r/choosingbeggars): if a company or an entity comes up to you offering "an opportunity to dress their shirt" in exchange for your time (money), brain (freedom), think twice: there should be no room for slavery in the world, both the real and the "coding" world.

## Wrapping up

This is it, for now, thank you for reading. Feel free to reach out to me with ideas and comments. This is my personal take on it, and as with any viewpoint, it's bound to be flawed. Stay tuned for a follow-up post I'll do to this one where I'll talk about examples of projects that are surviving to this day.
