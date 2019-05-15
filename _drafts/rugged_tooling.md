---
layout: post
title: "(DRAFT) The need for rugged tooling"
meta_description: "(DRAFT) The need for rugged tooling"
date: 2019-05-15
categories: [draft]
image: /assets/images/jp_404.jpg
caption: "Replace this, 2018"
---

/TODO

## Setup

What follows are my experiences of using the tool fro 10 October 2018 up until 15 May 2018
These are all the versions I had the chance to use between those dates, all of them pretty much updated around their release date: `6.4.2`,`6.4.4`,`6.5.2`,`6.5.3`,`6.6.1`,`6.6.1`,`6.7.1`,`6.7.2`,`6.7.3`,`6.7.4`,`7.0.4`,`7.0.6`,`7.0.7`,`7.0.9`.

Per working day I may run with the Postman client between 100 and 300 requests, depending on if it's "full-on" test sessions or if I'm doing setup and investigation work, in which case I won't use Postman as much.

This is also not taking into consideration the executions of the postman collections in a "Continuous Integration" fashion - via `newman` - I'll leave my experiences with it for a later post.

/TODO

## Typical work

## The good parts - beating Time constraints

The results I'm able to achieve with using Postman, in opposition to maintaining a typical automated checking suite - I would consider - where of benefit for the context of the project I was inserted into.

On a daily basis I was finding 2-3 meaningful bugs, per day - the feedback loop with developers was short, and, from experience, it was shorter taking a "Postman" approach, than a more standard one that Coding Testers tend to follow (Aka. QA Engineers) - where we tend to lose ourselves developing the automated check suite.

In a typical approach we tend to use some flavour of Gherkin and Cucumber library + a typical Programming Language + some Unit Test Libs + some REST libs, like Restassured. This approach takes tremendous amounts of time - valuable time which we're not spending experiencing and experimenting with the APIs and the services which we are supposed to be testing - and this is where using Postman gives a tactical advantage in projects where we're short on time or "releasing" and "pushing" on a weekly basis.

Because lately I'm usually dealing with what I call "monster" projects, where both the software being developed is complex and the delivery time-constraints are hardcore, I'm usually in "[Commando](TODO_RAID-ST_link)" mode most of my time - and it's invaluable for me and my team that I get to focus more on checking and testing activities - than code maintenance activities that come with making a framework. And since usually I'm a sole Tester in a small/medium development team - time spent testing is my most valuable time.

As for the volume of work of making execution of the check suite run as part of pipelines I would say the effort it's similar, with resource to `newman` in this case, where the tasks revolve around creating a couple of files that describe the Pipeline in code, dealing with issues when running it on the CI software, and then updating and maintaining the "test" pipeline. This work I'll also leave for another post.

## The ugly parts

/TODO

### Unmaintainable mess

"Branches/Forks" feature provided by Postman don't convince me. As someone who is used to working everyday with git, making multiple commits and a couple of pull requests per day (not counting those I make per week outside of work) I find Postman's "pre-fabric" offer of "Version control" and branching for the collections not trustworthy. At the very least what is offered solely via the Client App. Having had postman break (discussed in a point bellow) - and needing to share collections with muliple developers as well as having running them within a private CI environment with no connection to the "outer-world" - makes me adopt a stance where I have to maintain "by hand" several postman collection and environemtn files in a private company git repository - and it's a lot repetitive work with not a lot of straightforward options to automate and make it easier.

Another runner-up problem, the "works on my machine" situation: At one point I end up maintaining tons of files - some of them get deprecated quickly - and sharing with developers is incredibly stressful - no matter how much I try to make the collections and environment easily importable and "out-of-the-box working" after import - every single time it always feels like sharing them results in constant tiny rocks inside "my shoe" because it "works on my Postman" but not on my colleagues Postman.

### Slowness

Slowness, having between 10 and 20 different open collections, and sometimes a few of them with over 100 different specified requests, plus having around 10 environments defined, each of which can go up to 70 different variables leads me a lot of times to "micro"-frustration with over how Postman can be slow in terms of interactions,for example:

- Editing a variable in a given environment - you can most times see the lag between each character you type. Sometimes this lag got to, not kidding, 1 to 2 seconds.
- Editing a Request - same as above
- Switching between tabs of requests - same as above
- Opening folders withing collections - same as above

Input lag and visual lag are incredibly frustrating with postman, and tend to emotionally lead me to a state where I'm not trusting the tool I use. Can you picture the stress someone who is opening a whole in the street with a pneumatic hammer or someone who is cutting a block of wood if their tools don't work? Of course, if postman doesn't work, I don't risk losing a limb, but the stress of using a tool that doesn't feel "solid/consistent" is real.

/TODO-screenshot

### Break and dissapear bugs in sleeps

- On some versions - if you had coded a sleep in the pre-request - you could actually crash and make Postman "disappear" :
	- if for example you cancelled a Run via the Runner - while the Run was in this sleep
	- Or if you cancelled a single request - while the request was in this sleep

/TODO-screenshot

### Weird environment behavior

At one point, with loads of collections in the workspace, plus environments with tens of variables - editing a variable would sometimes edit another completely different variable, and the one I intended to edit remained the same. I tried to reproduce this by creating and importing an environment file with a few hundreds of variables, on a fresh workspace, but it wasn't reproducible. Also not a big chance of me sharing my "working" workspace - since there's tons of data that is private/confidential. I'm guessing it could be that my heavy-load workspace in Postman makes the app reach a point when the state of the app and it's memory start behaving in unpredictable ways. Something maybe for the postman folks to explore and experiment to make the app more reliable in extreme usage conditions.

/TODO-screenshot


### Better text editting for request related windows

I had the need during test sessions to edit multiple fields in, say, the JSON of a given request I'm working at any time - and I found myself copying and pasting from Postman and to Sublime and then, back, just to be able for example, to quickly indent the JSON, search and edit multiple fields at the same time, and write something with multiple active Carets. So in this sense, the text editor of requests could be a bit more powerful.

/TODO-screenshot

### No multiple edit of fields in requests and environment variables

Also the environment editing would benefit from a "bulk edit" view (similar to headers and parameters) where I can use a text editor to edit rapidly multiple environment variables.
It's frustating to edit multiple environment variables in a quick way - having to click input element for every variable in order to make it active, edit the variable, and at the end click Update - and if for some rease you edit multiple variables and forget to click Update - all the harduous work is gone, you have to repeat again.

/TODO-screenshot

### Conclusion

/TODO

Tools used in testing - should be TESTED - ruggedness, reliability, extreme usage, unexpected usage.

Also nice-to-have - easy "report bug" button - to report a bug - sending for example crash logs and others.
