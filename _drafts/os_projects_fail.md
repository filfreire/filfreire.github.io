---
layout: post
title: "(DRAFT) Why Opensource projects fail"
categories: [opensource, development, quality]
image: /assets/images/2018/12/toystory3.png
caption: "Toy Story 3, 2010"
---

> **Disclaimer**: this is a personal account based on my observations as a regular OSS contributor. Experience and observations will certainly vary from person to person.

Recently I've done an [internal session](TODO) at Adidas about the pros of following practices of some of the best opensource projects in a corporate environment, and how those deeply impact both the quality of the development process, and also in some ways the perceived quality by the end-users of the developed product.

In a summarized way, the points I mention in the talk are pretty much "no-brainers" for people who contribute or follow regularly to opensource projects:

- Tipically companies have a hidden (or visible) "ship fast or die mindset";
- Some companies defend some nasty concepts, with the excuse there's guaranteed sucess when (only) follow footsteps of giants (like Spotify, AWS, etc.);
- We fail to see that "opensource" "is all around us, it bind us" (like the Force in SW);
- We need the same rigour & code quality we see in the best OSS projects;
- We need to focus on 1 meaningful and important problem at a time;
- We need to aim for Sustainability and Maintainability (being agile does not mean being blazing fast and a good slave);
- "No time to test" is a myth;
- "No time to document" is a myth;
- Bug reports shouldn't be "apply template here" - they should be meaningfull;
- Testing in OSS is not "counting test cases or covering everything with a reactive nonmetal based checking library";
- OSS projects self-evaluate;
- Lessons of Motivation, happiness and drama in OSS - these are way bigger than in the corporate world;


The basic idea to wrap up that talk was that OSS projects live, survive and adapt longer: because of quality, OSS development described "slowness" and it's development model being unfit by the corporate world is also a myth, and we can change a bit in our workplace everyday.


At one point a dear colleague of mine mentioned that it would be interesting to see the reverse of the coin: why do some OSS projects fail, fall into abandonment, and how some of them manage to survive impending failure to this day. I think these points are as important to go through as are the more "positive, we can change the corporate" world points, so what follows in this post is a collection of observations I've made over time to directly touch theses topics of the "failure" side of things.


## Emotional motivation for abandonment

I believe that one reason projects get abandoned or fail is because of "life" and not necessarily because the maintainer is a crappy or evil human. Its most times because of the reasons you'll find maintainers tipically writing about. Here's an interesting [example read](TODO).

Tinkering and coming up with a piece of code and putting it online for the world to see is one thing. Making it maintainable is another thing. Maintaining it over a prolonged period of time is yet another thing. OSS is hard-work sometimes for simple reasons: life, for better or worst, gets in the way and finds a different way ([Jurassic Park pun unintended](TODO)).

- You come home tired from work;
- You want to spend time with your family;
- You want to spend time with your other hobbies besides programming;
- You want to go outside and do something;
- You can't see another computer in front of you after hours of tackling with one at work;
- ...

All of these are normal. I personally believe we should never bash people who stop maintaining stuff for any personal reason whatsoever. Life is hard for everyone. If for any reason you think the maintainer is not being responsible, don't bash the maintainer, go the other way, fork the project, start your own branches with your ideas and improvements, direct other people towards your branch, and do things in a way that you're still apreciating someone else's initial work.

## Set for abandonment

**The documentation is garbage** - for me it's an indicator project is from the start not set for maintainability - It's a bit of a dirty hobby for me, but I do this over time: when I see a project doesn't have a readme, or the readme clearly misses to say how I can build and use the project on my local machine, I open an issue exactly to tackle that. Just to give you an idea that this is not an isolate problem: Here's a list of all the issues I've opened in this fashion for diverse projects as of the day I'm writing this post:

-- (TODO)

**Documentation is there, but to build on your machine you need sorcery, and tackle build errors that "stackoverflow will only have an answer in 2-3 years"**. The next logical step after documenting it is: make it run in a CI solution. There are countless available, from [Travis](TODO) to [CircleCI](TODO), free for opensource projects, and yet, sometimes people just avoid these, in their minds "oh I don't need this, I can build fine on my own machine". The thing is your machine is not my machine or the person's next door machine. The easiest way to guarantee that the person next door will have a good chance of building your project locally is plainly making it build on CI. It's confusing, and maybe for some people it'll take 5 minutes for other people 5 days, but the benefits are there once it's set up: chances are better for potential contributors to be able to build your project locally or by setting it to build on CI you'll run into blocking points that a future contributor will run.

**Last commit made in 1942, before going on covert-ops mission in north africa**. This point is a no brainer. If the project hasn't been updated for years, If the CI seems abandoned, if there are tons of issues or pull-requests open and not a single reply from the maintainer - (TODO)

## Set for survival

**Replying soon, reviewing soon, merging soon**. Recently a colleague of mine opened an interesting PR in [danger](TODO) repo. In a matter of minutes the PR was reviewd, merged, and my colleague invited to be a maintainer, with the premise of this [policy](TODO);

**Pay contributors in money, not in exposure**: Some of the projects I've contributed towards for example are set in a way that you can pay contributors to help you fix or develop issues that affect you. I think this is fine. There are a couple of strategies for this:

- from a "no-human-manager" and projects are financed in a way anyone can contribute and be monetary rewarded, an approach you'll find in contexts like [zerocracy](TODO);
- to a "pay for an expert and active contributor of a project for a tailor-made adaptation of the project, like you'll find in some funded OSS projects like [geonetwork](TODO);

## Surviving to this day

**Involving more people who are deeply interested** (TODO)

**If it's not solving a meaningful problem - scrap it and work on one that does** - and again involve people (TODO)

**What grep and kubernetes have in common** (TODO)

## Wrapping up

(TODO)