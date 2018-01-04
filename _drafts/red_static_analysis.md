# What is the colour of static analysis?
## TL;DR: 
I think it should be red. 
Static analysis is amazingly useful - a lot of issues that I’m used professionally to see caught in CRs are automatically prevented if the build fails with static analysis.

## Quick-intro


## What we usually have
From my professional experience projects usually have static analysis in them but in practice it's not adding much value to the project. It spills out tons of warnings on build time, warnings that are in turn ignored often because we as developers invest our time in making a build green and we usually only care if the tests that run during build or integration break. We never give much aprecciation to the warnings yelled out by the static analysis. Worst and typical case-scenario, at some point in time we actually deactivate static analysis and similar automated checks because "we're not getting anything out of it".

So in summary, it's there but it's the same as if it weren't. And yes some may say, oh but when we have the time we'll handle it, sometimes I see the warnings and act on them. Sometimes is not good enough. It's either part of the development proccess and is an active and integral part of it, or it's not really doing anything and it's there just for show. I'd recommend in the latter case, don't even bother adding static analysis then. Remove it. You haven't been using 

## What we should have

Simple: static/code analysis should break a build the same way unit tests do. If you get a code style warning, a static analysis yellow message, a code coverage difference between minimum and actual, your build should break.
Will it slow you down? Yes. At first. But the effort to make the development process clear and breaking on analysis warnings bears a lot of fruit on the long run. Read on.


## What we get in return

* We get code that's uniform throughout the code base, there are no layers of different programer's code that are unique and distinct in a whole project;
* We avoid a lot of small issues, be them of syntax sugar, or styling, or actual code smells that are usually picked up at code review;
* Codebase is easier to maintain and hop into by new people. Anyone new doesn't need to waste a lot of reviewers and maintainers time because when they submit the code, the code itself is already obeying the set of rules that everyone obeys;
* Code and Style Guidelines are actually met. Always. Because it's enforced on any contributor - they're alive and not some documentation that some people read and some people don't;
* We invest our time better during code review, we worry less about typical stuff and focus more on what the code is trying to achieve versus what we proposed to solve or create;

There should be more points, but these are the ones I can relate to at the time of writing.



## Oh but "It's impossible to have that on a real agile super dynamic fast-paced scrum enviroment of high concurrent software"
First, not all of the stuff we build will ever be that important that we'll need to think about shipping fast.
I worked at companies with "said" high volume of messages and critical business, and actual companies with a ton of processing volume, critical, if something goes wrong you're fired not because you're boss has an excuse to but you caused the company to lose more than hundreds of thousands of dollars.

With that said. We use the velocity and ship-to-market speed as an excuse to ignore or have dummy static analysis that is worthless.. It shouldn't be the case.

Ship-to-market speed should never be an excuse for poor software. Software quality should be decent enough. I'm not advocating perfection, but at least some hygiene. Not all people floss everyday. Yet it is one of the things dentists keep advocating all the time that actually makes a lot of difference on the long run.

Static analysis being red and not yellow gives a project that minimal ammount of hygiene on the development process. Same way unit tests and other types of tests do. The same way something like exploratory testing  does. But different hygiene practices have different granularities and different purposes. You could live your entire life not flossing, or not brushing teeth, or not eating healthy food. That won't stop you from living a good life on many fronts. But on some fronts, that make a lot of difference on the long run, I'll tell you what the doctor tells everyone: you should try to do this.




## Examples it works in practice

## Extra: Are you starting a project in Java?

## Other languages



