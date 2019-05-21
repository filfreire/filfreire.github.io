---
layout: post
title: "Frail and cast-iron tools - Episode 1"
meta_description: "Frail and cast-iron tools - Episode 1"
date: 2019-05-22
categories: [tools, testing, api testing, postman, personal experience]
image: /assets/images/2019/05/deltaforce.jpg
caption: "Delta Force, 1986"
---

> Disclaimer: This post is about my personal experience using a specific tool, [Postman](https://www.getpostman.com/). It's not a tutorial. It's not a paid or endorsed review. It's a recollection of my experiences, feelings, frustrations and a flawed portrait of my user experience with the tool, from a software tester point of view. That said, I should say, no matter how much I might sound negative at some points, I prefer to do so and stay true to myself as a tester, instead of making a blog post of shallow "praise and wonder". Read on!

I have this subconscious feeling that every day there's a new "testing" tool being pushed on the market advertised as the killer tool, perfect, will solve all my problems. But, this is not another post to add to the narrative that there is such a thing called "Automated Testing". You can automated checking, but you can't automate creative activities such as programming and experiential testing.

Accompanying the subconscious feeling of fancy software tools being regurgitated to the testing community every once in a while is also the dread I have with any new tool that is announced - If I decide to use this tool:
- When will it expectedly start failing me (since it's usually only a matter of time)?
- When will it betray me over some unexpected complex testing situation?
- When is this tool gonna break down on me? Is it simple? Will it always work for the purpose I intend to give it?
- ...

In the software testing craft, with my experience, I believe not a lot of tools respond positively to all these questions I wrote before, but, picking one that has been my tool of use lately, I find **Postman** is not one of these "fancy new tools", in the sense it's established and seems to have a growing user base.

A lot of people and a lot of companies use it or have an opinion formed on it with substance and foundation. I quick search on Twitter, for example, and I saw what seemed quite a few users to whom the tool seems really useful. What I've also found with time was that Postman, though became invaluable to me with its usage, is far from being a silver bullet, and also is not exactly a tool I can actively "depend my life on" on the same way I depend on software like bash, git, vim or Sublime. What follows are my personal experiences (and frustrations) of using the Postman (Free) Native App, from a Coding Tester user's perspective.

## Setup

So, let's start off, timewise, this post is about my experience using the app from 10 October 2018 up until 16 May 2018. I've used the app before and of course I've been using after the last date mentioned here, but for the context of this post - I'll only talk about the issues I found of which I have some data about.

I've used Postman consistently between these dates, and these are all the versions I had the chance to use, all of them pretty much updated around their release date: `6.4.2`, `6.4.4`, `6.5.2`, `6.5.3`, `6.6.1`, `6.6.1`, `6.7.1`, `6.7.2`, `6.7.3`, `6.7.4`, `7.0.4`, `7.0.6`, `7.0.7`, `7.0.9`, `7.1.0` and even `7.1.1-canary02`.

Per working day I may have executed with the Postman client between 100 and 300 requests, depending on if it's "full-on" test sessions or if I'm doing setup and investigation tasks, in which case I won't issue requests on Postman as much.

This is also not taking into consideration the executions of the postman collections locally with scripts or remotely in some "Continuous Integration" fashion - via `newman` - I'll leave my experiences with that for a later post. You also won't find any review in this post with regards to the different paid solutions that exist for Postman - I'm oblivious to those.

## What I liked the most

### Beating Complexity and Time constraints

> As a tester: Time spent testing is my most valuable time.

The testing efforts I was able to achieve with the aid of Postman, in opposition to maintaining a typical automated checking suite - I would consider - were of immense benefit for the context of the project and teams I was inserted into:

- Since the beginning of the year, with the aid of Postman as a tool, I was finding 2-3 meaningful and important bugs, per day, and I've consistently never had a week without finding a bug;
- the feedback loop with developers felt shorter than usual, between implementation and deployment time and experiential testing stages;

It felt tremendously quicker taking a "Postman" approach, than a more standard one that Coding Testers tend to follow (Aka. QA Engineers) - where we tend to lose ourselves developing the automated check suite. In a typical approach, we tend to use some flavor of Gherkin and Cucumber library + a typical Programming Language + some Unit Test Libs + some REST libs, like Restassured. This approach takes tremendous amounts of time - valuable time which we're not spending experiencing and experimenting with the APIs and the services which we are supposed to be testing - and this is where using Postman gives a tactical advantage in projects where we're short on time or "releasing" and "pushing" on a weekly basis.

Because lately I'm usually dealing with what I call ["monster"](https://filfreire.com/posts/asymmetric_warfare) projects, where both the software being developed is complex and the delivery time-constraints are hardcore, I'm usually in "[Commando](https://filfreire.com/posts/asymmetric_warfare)" mode most of my time - and it's invaluable for me and my team that I get to focus more on checking and testing activities - than code maintenance activities that come with making a framework.

As for the volume of work of making execution of the automated checks, in this case, coded as Postman collections, run as part of pipelines I would say the effort was similar to a more default approach, using a containerized execution of the checks with `newman`, and in this case, where the typical tasks revolve around
- creating a couple of files that describe the pipeline in code (ex. Jenkinsfiles);
- dealing with issues when running it on the CI software;
- updating and maintaining the "test" pipeline. A more deep description of this setup I'll also leave for another post.


### Straight to the point

I can only talk from my personal experience, but I like a lot of what I've seen:
 - documentation-wise Postman and (and `newman`) are pretty complete for anyone who wants to use the tool quickly, for example, to quickly set up some API automated checks and start testing, or to quickly run the checks in a containerized fashion - from personal experience, not a lot of tools that testers can use have this type of straightforward practical documentation on using the tool and configuring it.
 - they seem to provide good means for the community to interact with questions or report bugs, all in a fairly transparent fashion, either via Github, their hosted forum, and even Twitter. Their involvement with the community appears to be way deeper and "interesting" in comparison to a lot of other tool makers out there. I can count with the fingers of one hand the number of testing-related tools I've used who also have a similar interest in reaching out and helping the community, no matter how many people they employ.
 - even though they mention the term "automated testing" in their white paper and in some other places, which for those who follow my blog, already know what I think of those two words put together - they don't seem to bombard people and market the tool as a replacement of skilled craftsman testers, or a replacement of other automated checking tools - instead they mainly position themselves for what they actually are - an API Development Environment and a pretty good one at that, with options to have some of it deployed in the cloud with some more automation - and I think this tells more about the people behind the development of the tool than the typical cynical "snake oil" marketing schemes you find in most automated checking tools, or test-case management tools, and so on.

 Picking again on this last point, at least from what I've seen, and I might have missed something, they distance themselves on a practical level from other entities which are profiting from people's ignorance in the value of testing - and that is commendable.


### Folks over at Postman seem to care

Another important mention within this topic is, around the last days of my described experience, related to one of the latest versions of Postman, when I found what seems like a critical bug:

> Request search feature near the Collection and History tab started displaying completely unrelated requests to my search query.

Here are the links where you can find more about it: [Github issue](https://github.com/postmanlabs/postman-app-support/issues/6524) and [Twitter](https://Twitter.com/filrfreire/status/1129066967590158336).

When I was preparing the draft of this post, I had around the same time discovered the bug - so I put it under the "Stuff I did not like" section of the post. But it turns out that this issue for me ended up as a positive and happy note: the folks over at Postman noticed my tweet and my bug description, replied promptly and kindly, and did catch up and follow up work with regards to the bug. At one point they said in the Github ticket they managed to reproduce the bug and would issue a fix for it soon - and they did, the issue was solved and closed in 5 days time. You can even find it listed in on Postman's version [`7.1.1` release notes](https://www.getpostman.com/downloads/release-notes).

All of this taking into account they could have ignored the found bug since I'm a "non-paying" user, and not have invested time into it. A lot of software tool makers get to a point where they're up in their big towers, to not say something worse, and simply don't care about bugs reported by the community, but Postman seems to be taking the road of actually caring.

## What I did not like

Now, not everything is sunshine and butterflies - it's always a matter of time whilst using a tool until you find a few of its shortcomings, especially since my daily job is hunting down for bugs. Here are the issues that have stuck with me after all of this time of actively using Postman.

### Slowness

If there's one thing I can say with a certainty above all is else, it's that after a certain point of usage, which I can't exactly pinpoint when it began, I've started experiencing and still experience slowness, both in terms of visual lag and also of input lag.

I've reached a state of having between 10 and 20 different active collections (and way  more closed/archived or in other workspaces), and sometimes a few of them with over 100 different specified requests in different folders. Added to this is having around 10 test Postman environments defined, each of which can go up to 70 different environment variables, all of which leads me a lot of times to "micro"-frustration with over how Postman can be slow in terms of interactions, for example:

- Editing a variable in a given Postman environment - you can most times see the lag between each character you type. Sometimes this lag got to, not kidding, 1 to 2 seconds.
- Editing a Request - same as above
- Switching between tabs of requests - noticeable visual lag
- Opening pre-request or test tabs - same as above
- Opening "code" modal to download cUrl format of requests - same as above
- Opening folders withing collections - same as above

Input lag and visual lag get to a point where they are incredibly frustrating to deal with when using Postman, and tend to emotionally lead me to a state where I'm not trusting the tool I use. Can you picture the stress someone who is opening a hole in the street with a pneumatic hammer or someone who is cutting a block of wood if their tools don't work? Of course, if Postman doesn't work, I don't risk losing a limb, but the stress of using a tool that doesn't feel "solid/consistent" is real.

I understand this might come to be the case a lot of times taking into account the underlying way Postman app is built, maybe suffering from the same issues other Electron/Chrome-based "native" apps have - they fight for resources with "Chrome"-like apps - so a few open Chrome tabs, plus a few team spaces open in Slack "native" client ([which is also far for perfect in terms of input and visual performance](https://www.reddit.com/r/Slack/comments/9h4t9k/slack_macos_client_freezes_slowdowns_and_visual/)), and added to that Postman - I get it - I've gotten used to having input and visual lag in those conditions - but I truly believe something needs to be done so this is not the case.

I never have to worry about Sublime, vim, bash or any typical Unix-commands not working, they just work, "instantly", all the time, "perfectly", and I use them every day - and I know comparison isn't necessarily fair - but taking into account the larger public reach that Postman is getting - I would be impressed if their native app would take an approach of making the user experience of using the tool as rugged and dependable, and "snap"-performance as other software tools we've all grown accustomed too and we depend on. It would maybe take a big investment and a lot of deep testing by the folks who make Postman - but I for one think it would pay off for them.

### "Break and disappear" when canceling requests/runs

Unlike with testing frontend applications, say with some programming language and a Selenium library, there's no elegant way of doing "fluent waits" in any Postman pre-request or test script part, that I know off. Postman's offer to add some wait between requests also wasn't really helpful because sometimes I just needed to wait before a specific request and not all of the requests in a given run.

So I found that, on some versions, if you had a hard-coded sleep/wait, say, in on pre-request in a fashion like this one:

```
console.log("Beginning wait...");
setTimeout(function(){console.log("Finished waiting...")}, 60*1000); // 1 minute wait
```

you could actually crash the Postman App and make it disappear, specifically if you were doing one of the following:

1) You canceled a "Run" via the "Postman Runner" - while the Run was in this sleep;
2) Or if you canceled a single request - while the request was in this sleep;

I didn't have the chance to register in which versions each flavor of the problem happened. I remember that for some both issues manifested, and for latest versions, I've only caught the second more often.

The worst for me is that I've grown accustomed to this failure - so no I subconsciously try to foresee when I might have done something wrong that would force to cancel the request or the collection run - and I just stop myself from doing that. It's not ideal.

### Weird environment behavior

At one point, with loads of collections in the workspace, plus environments with tens of variables - editing a variable through the quick "eye" menu of the environment would sometimes edit another completely different variable a bit bellow in the variable list of that environment, and the one I intended to edit remained the same.

I tried to reproduce this by creating and importing an environment file I generated with a few hundreds of Postman environment variables, on a fresh workspace, but the behavior, for some reason wasn't reproducible. Even worse was that it was always reproduced by accident. I followed someone's suggestion and I've been keeping the number of active Postman collections, environments and open tabs at any time in a workspace to a minimum since it could be a memory-filling-up leading to unexpected behavior kind of issue, but it's hard to say.

From a user experience perspective it was around the same time I was starting to see this behavior that I started to think I was hitting some sort of limit of what the Postman Native app could do as a tool, and around the same time the veil started to disappear and the honeymoon period with the app was over.

Sadly there's also not a big chance of me sharing my "working" workspace - to help reproduce this, since there is data I cannot share. Yet another thing maybe for the folks who develop Postman to explore and experiment to make the native app more reliable in what felt like "extreme" usage conditions.

### Lack of good "power-user" text editing for request views

I have constantly the need during test sessions to edit multiple fields in, say, the JSON of a given request I'm working at any time.

And every day it's the same story: I find myself copying and pasting the text from Postman to Sublime and then back, just to be able for example, to quickly indent the JSON, or search and edit multiple fields at the same time, and to write something in multiple places with multiple active Carets.

So in this sense, I think the text editor part of requests in Postman could be a bit more powerful. I'm not suggesting as powerful as, say, vim or Sublime can be, but just powerful enough to allow me to not have the need to leave the tool when I need to make complex edits.

### Harsh editing of environment variables

Similar to the previous point, the environment editing would benefit from a "bulk edit" view (similar to the one found in request's headers and parameters) where I can use a text editor to edit rapidly multiple environment variables.

It's frustrating to edit multiple environment variables and there's no quick way to do it - I have instead to click on an input element for every single variable in order to make it active, edit the variable, and at the end click Update - and if for some reason you edit multiple variables and forget to click Update - all the arduous work is gone, you have to repeat again. So for example, a natural thing to do in the world of "continuous saves", clicking "Esc" on the keyboard while editing the environment will make you lose all your environment editing work that was in progress - which for me has been infuriating quite a few times.

One of Postman's alternatives, [Insomnia](https://insomnia.rest/) seems to have surpassed this by allowing to edit environments as JSON files (which is the same format of the exported environments in Postman). And though Insomnia has others bugs, for example, related environments compatibility with exported ones from Postman, I would suggest adding the possibility to edit environments in a similar fashion.

### Version control and sharing seem shady

The "Branches/Forks" feature provided by Postman hasn't **yet** convinced me. As someone who is used to working every day with Git, making multiple commits and a couple of pull requests per day (not counting those I make per week outside of work), as well as performing a couple of code reviews: I find Postman's "pre-fabric" offer of "Version control" and branching for the collections, from a user experience perspective, not trustworthy... **yet**.

I say **yet** for 2 reasons:

- Sometimes I tried merging simple changes of a collection fork into the "master" collection -  and for simple changes, it worked decently well;
- Sometimes I tried merging complex changes to a collection - and it sucked - the visual diff was all over the place and not to a level where, by comparison, Github's visual diff is;

Having had Postman break/freeze (discussed in a point above) - and needing to share collections with multiple developers as well as having running them within a private CI environment with no connection to the "outer-world" - makes me adopt a stance where I have to preventively maintain, "by hand", several Postman collection and environment files in a private git repository - just so I don't risk losing it all, and have a safeguard to share them with developers in case of need - and the maintenance of it all is a lot repetitive work with not a lot of straightforward options to automate and make it easier.

Another runner-up problem is the "works on my machine" situation: At one point I end up maintaining tons of collection and environment files - some of them get deprecated quickly - and sharing with developers is incredibly stressful - no matter how much I try to make the collections and environment easily importable and "out-of-the-box working" after import - every single time it always feels like sharing the results in constant tiny rocks inside "my shoe" because it "works on my Postman" but not on my colleagues Postman client.

### Environment exporting is a pain

This really, as Peter Griffin would put it, "grinds my gears": every time I try to export my environments it's always a stressful gamble.

I feel the need to export the file with the initial values - and Postman provides. Sometimes, on the other hand, I would like to export the file with the current values - and Postman "doesn't care" and doesn't seem to provide an apparent or easy way for me to do this. And not once, never, did I ever need to export the environment variables that are only "created" via pre-requests or tests - which get populated as Current values in the environment, and once exported - turn out as empty value variables in the exported JSON. Usefulness for these: zero. So why have them there?

## Conclusion

As inspiration for this post - I remembered of a few sound engineers, electricians and cable technicians whom I've interacted with throughout life - they all had an inspiring organized toolset, every tool had a purpose, some tools where indeed expensive, but were likewise solid and rugged, and it always seemed they were an trusty extension of the person using them, who got something done way faster than anything I could do by myself with my wannabe toolbox of cheap screwdrivers and such. For some, it will seem like a cheesy analogy, but to me as a Tester who also does code, there's a certain charm with the kind of professionals who cultivate their knowledge, as well their tool usage techniques and their tool choices. So, as a wrap-up of this post, I'll underline one point:
Tools that are used to aid testing efforts: should be **TESTED** to a great extent.

As a tester, I usually pick my tools based on ruggedness and reliability, especially when it comes to supporting extreme and unexpected usage.
Maybe folks who develop Postman tested it to an extent where the common default user would have little reason to complain, but to me, it makes sense that at some point, a move in the direction of making the software one produces more reliable and "rugged" is a winner's move in my book. So if you're a tool maker and you're reading this - invest in deep testing of your developed products to a greater extent. I sincerely believe it pays off, even after the point where you have a consolidated user base - it doesn't mean anything if a part of that user base remains with your tool because they adapted to the tools flaws and can't find anything better.

If you're one of the folks who develop the [Postman Native app](https://www.getpostman.com/downloads/): You have my appreciation and respect.

Thank you for reading and stay tuned for the next episode :-)