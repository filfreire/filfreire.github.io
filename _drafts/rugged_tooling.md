---
layout: post
title: "(DRAFT) The need for rugged tooling"
meta_description: "(DRAFT) The need for rugged tooling"
date: 2019-05-15
categories: [draft]
image: /assets/images/jp_404.jpg
caption: "Replace this, 2018"
---

As inspiration for this post - I remembered the electricians and cable technicians I've interacted with throughout life - they all had an inspiring organized tool set, every tool had a purpose, some tools where indeed expensive, but were solid and rugged, a it always seemed they were an trusthy extension of the person using them, who got something done way faster than anything on I could do by myself with my wannabe toolbox of cheap screwdrivers and such.

I have this subconscious feeling that everyday there's a new "testing" tool being pushed on the market advertised as the killer tool, perfect, will solve all my problems.

Accompanying the subconscious feeling of fancy software tools being regurgitated to the testing community every once in a while is also the dread I have with any new tool that is annouced: If I decide to use this tool, when will it expectedly start failing me? When will it betray me over some unexpected complex testing situation?  When is this tool gona break down on me? Is it simple? Will it always work for the purpose I intend to give it? ...


In the software testing craft, with my experience, I believe not a lot of tools respond positively to these questions I posed before, but, picking one that has been my tool of use lately, I find Postman is not one of these "fancy new tools", in the sense it's established and seems to have a growing user base. A lot of people and a lot of companies use it, or have an opinion formed on it with substance and foundation. I quick search on twitter, for example, and I saw what seemed quite a few users to whom the tool seems really useful.

What I've also found with time was that Postman not a silver bullet, far from it, and also is not exactly a tool I can actively "depend my life on" on the same way I depend on software like bash, git, vim or Sublime.

What follows are my personal experiences (and frustrations) of using the Postman Free Native App, from a Coding Tester user's perspective.

I've used this app from 10 October 2018 up until 16 May 2018.
I've used it consistently between these dates, and these are all the versions I had the chance to use, all of them pretty much updated around their release date: `6.4.2`, `6.4.4`, `6.5.2`, `6.5.3`, `6.6.1`, `6.6.1`, `6.7.1`, `6.7.2`, `6.7.3`, `6.7.4`, `7.0.4`, `7.0.6`, `7.0.7`, `7.0.9`, `7.1.0` and even `7.1.1-canary02`.

Per working day I may have executed with the Postman client between 100 and 300 requests, depending on if it's "full-on" test sessions or if I'm doing setup and investigation taks, in which case I won't issue requests on Postman as much.

This is also not taking into consideration the executions of the postman collections in a "Continuous Integration" fashion - via `newman` - I'll leave my experiences with it for a later post. You also won't find any review in this post with regards to the different paid solutions that exist for Postman - I'm oblivious to those.


## The good part
### beating Complexity and Time constraints

> As a tester: Time spent testing is my most valuable time.

The testing efforts I was able to achieve with the aid Postman, in opposition to maintaining a typical automated checking suite - I would consider - where of benefit for the context of the project I was inserted into:

- with the aid of Postman as a tool, I was finding 2-3 meaningful and important bugs, per day;
- the feedback loop with developers felt shorter than usual, between implementation and deployement time and experiencial testing stages;

It felt shorter taking a "Postman" approach, than a more standard one that Coding Testers tend to follow (Aka. QA Engineers) - where we tend to lose ourselves developing the automated check suite. In a typical approach we tend to use some flavour of Gherkin and Cucumber library + a typical Programming Language + some Unit Test Libs + some REST libs, like Restassured. This approach takes tremendous amounts of time - valuable time which we're not spending experiencing and experimenting with the APIs and the services which we are supposed to be testing - and this is where using Postman gives a tactical advantage in projects where we're short on time or "releasing" and "pushing" on a weekly basis.

Because lately I'm usually dealing with what I call ["monster"](TODO) projects, where both the software being developed is complex and the delivery time-constraints are hardcore, I'm usually in "[Commando](TODO_RAID-ST_link)" mode most of my time - and it's invaluable for me and my team that I get to focus more on checking and testing activities - than code maintenance activities that come with making a framework.

As for the volume of work of making execution of the automated checks, in this case, coded as Postman collections, run as part of pipelines I would say the effort was similar to a more default approach, using a containerized execution of the checks with `newman`, and in this case, where the typical tasks revolve around
- creating a couple of files that describe the pipeline in code (ex. Jenkinsfiles);
- dealing with issues when running it on the CI software;
- updating and maintaining the "test" pipeline. A more indeep description of this setup I'll also leave for another post.

## The "not so good" parts


### Slowness

If there's one thing I can say with certainty above all is else, it's that after a certain point, which I can exaclty pinpoint when, I've started experiencing and still experience slowness, both visual lag and input lag.

I've reached a state of having between 10 and 20 different active collections (and a couple other more closed/archived or in other workspaces), and sometimes a few of them with over 100 different specified requests in different folders, plus having around 10 test postman environments defined, each of which can go up to 70 different environment variables, all of which leads me a lot of times to "micro"-frustration with over how Postman can be slow in terms of interactions, for example:

- Editing a variable in a given postman environment - you can most times see the lag between each character you type. Sometimes this lag got to, not kidding, 1 to 2 seconds.
- Editing a Request - same as above
- Switching between tabs of requests - noticeable visual lag
- Opening pre-request or test tabs - same as above
- Opening "code" modal to download cUrl format of requests - same as above
- Opening folders withing collections - same as above

Input lag and visual lag get to a point where they are incredibly frustrating to deal with when using postman, and tend to emotionally lead me to a state where I'm not trusting the tool I use. Can you picture the stress someone who is opening a whole in the street with a pneumatic hammer or someone who is cutting a block of wood if their tools don't work? Of course, if postman doesn't work, I don't risk losing a limb, but the stress of using a tool that doesn't feel "solid/consistent" is real.

I understand this might come to be the case taking into account the underlying way postman is built, suffering from the same issues other Electron/Chrome based "native" apps have - they fight for resources with Chrome - so a few open Chrome tabs, plus a few team spaces open in Slack "native" client, and added to that Postman - I get it - I've gotten used to having input and visual lag in those conditions - but I truly believe something needs to be done so this is not the case.

I never have to worry about Sublime, vim, bash or any typical Unix-commands not working, they just do, all the time, "perfectly", and I use them everyday - and I know maybe comparison isn't fair - but taking into account the larger public reach that Postman is getting - I would be impressed if their native app would take an approach of making the user experience of using the tool as rugged and dependable, and "snap"-performance as other software tools we've all grown accostumed too and we depend on. It would maybe take a big investment and a lot of deep testing by the folks who make Postman - but I for one think it would pay off for them.

### Break and dissapear when cancelling requests/runs

Unlike with testing frontend applications, say with some programming language and with resource to a Selenium library, there's no elegant way of doing "fluent waits" in any Postman pre-request or test script part, that I know off. Postman's offer to add some wait between requests also wasn't really helpful because sometimes I just needed to wait before a specific request, and not all of the requests in a given run.

So I found that, on some versions, if you had a hard-coded sleep/wait, say, in on pre-request in a fashion like this one:

```
console.log("Beginning wait...");
setTimeout(function(){console.log("Finished waiting...")}, 60*1000); // 1 minute wait
```

you could actually crash the Postman App and make it disappear, speficially if you where doing one of the following:
1) You cancelled a "Run" via the "Postman Runner" - while the Run was in this sleep;
2) Or if you cancelled a single request - while the request was in this sleep;

I didn't have the chance to register in which versions each flavour of the problem happened. I remember that for some both issues manifested, and for latest versions, I've only caught the second more often.

The worst for me is that I've grown accostumed to this failure - so no I subconsciously try to foresee when I might have done something wrong that would force to cancel the request or the collection run - and I just stop myself from doing that. It's not ideal.

### Weird environment behavior

At one point, with loads of collections in the workspace, plus environments with tens of variables - editing a variable would sometimes edit another completely different variable, and the one I intended to edit remained the same.

I tried to reproduce this by creating and importing an environment file I generated with a few hundreds of postman environment variables, on a fresh workspace, but the behavior, for some reason wasn't reproducible. Even worse was that it was always reproduced by accident. I followed someone's suggestion and I've been keeping the number of active postman collections, environments and open tabs at any time in a workspace to a minimum, since it could be a memory-filling-up leading to unexpected behavior kind of issue, but it's hard to say.

From a user experience perspective it was around the same time I was starting to see this behavior that I started to think I was hitting some sort of limit of what the Postman Native app could do as a tool, and around the same time the veil started to dissapear and the honeymoon period with the app was over.

Sadly there's also not a big chance of me sharing my "working" workspace - to help reproduce this, since there's tons of data that is private, and I can't share. Yet another thing maybe for the folks who develop Postman to explore and experiment to make the native app more reliable in what felt like "extreme" usage conditions.


### Lack of good text editting for request views

I have and had the need during test sessions to edit multiple fields in, say, the JSON of a given request I'm working at any time.

And everyday it's the same story: I find myself copying and pasting from Postman and to Sublime and then back, just to be able for example, to quickly indent the JSON, or search and edit multiple fields at the same time, and write something with multiple active Carets.

So in this sense, I think the text editor part of requests in Postman could be a bit more powerful.


### Harsh editing of environment variables

Similar to the previous point, the environment editing would benefit from a "bulk edit" view (similar to the one found in request's headers and parameters) where I can use a text editor to edit rapidly multiple environment variables.

It's frustating to edit multiple environment variables in a quick way - having to click input element for every variable in order to make it active, edit the variable, and at the end click Update - and if for some rease you edit multiple variables and forget to click Update - all the harduous work is gone, you have to repeat again.

### Search stopped working


Around the last days of my described experience, with a latest verion of Postman, what seems like a critical bug to me, might have been introduced:

> Request search feature near the Collection and History tab started displaying completely unrelated requests to my search query.

Here are the links where you can find more about it: [github issue](https://github.com/postmanlabs/postman-app-support/issues/6524) and [twitter](https://twitter.com/filrfreire/status/1129066967590158336).

### Version control and sharing are shaddy

The "Branches/Forks" feature provided by Postman hasn't **yet** convince me. As someone who is used to working everyday with git, making multiple commits and a couple of pull requests per day (not counting those I make per week outside of work), as well as performing a couple of code reviews: I find Postman's "pre-fabric" offer of "Version control" and branching for the collections, from a user experience perspective, not trustworthy... **yet**.

I say **yet** for 2 reasons:

- Sometimes I tried merging simple changes of a collection fork into the "master" collection -  and for simple changes it worked decently well, kudos;
- Sometimes I tried merging complex changes to a collection - and it sucked - the visual diff was all over the place and not to a level where, by comparison, Github's visual diff is;

Having had postman break/freeze (discussed in a point above) - and needing to share collections with muliple developers as well as having running them within a private CI environment with no connection to the "outer-world" - makes me adopt a stance where I have to preventively maintain, "by hand", several postman collection and environment files in a private git repository - just so I don't risk losing it all, and have a safeguard to share them with developers in case of need - and the maintenance of it all is a lot repetitive work with not a lot of straightforward options to automate and make it easier.

Another runner-up problem is the "works on my machine" situation: At one point I end up maintaining tons of collection and environemtn files - some of them get deprecated quickly - and sharing with developers is incredibly stressful - no matter how much I try to make the collections and environment easily importable and "out-of-the-box working" after import - every single time it always feels like sharing them results in constant tiny rocks inside "my shoe" because it "works on my Postman" but not on my colleagues Postman.


### Magical world of environment exporting is a pain

This really, as Peter Griffin would put it, "grinds my gears": everytime I try to export my environments it's always a gamble.

I feel the need to export the file with the initial values - and Postman provides.

Sometimes on the other hand I would like to export the file with the current values - and Postman "doesn't care" and doesn't seem to provide an apparent or easy way for me to do this.

And not once, never, did I ever need to export the environment variables that are only "created" via pre-requests or tests - which get populated as Current values in the environment, and once exported - turn out as empty value variables in the exported json. Usefulness for these: zero. So why have them there?

### Conclusion



Tools used in testing - should be TESTED - ruggedness, reliability, extreme usage, unexpected usage.

Also nice-to-have - easy "report bug" button - to report a bug - sending for example crash logs and others.
