---
layout: post
title: "Frail and cast-iron tools - Episode 2"
description: "A portrait of my user experience with the k6 tool"
meta_description: "A portrait of my user experience with the k6 tool"
date: 2021-04-12
categories: [tools, testing, load testing, k6, personal experience]
image: /assets/images/2021/04/first-blood.jpg
image_alt: a movie still from First Blood 1982
caption: "First Blood, 1982"
---

It's been almost a year since my [first *Frail and cast-iron tools* episode](https://filfreire.com/posts/frail_castiron_ep1) where I wrote about my personal experience with [Postman](https://www.postman.com/) and I've decided to do a new follow-up episode dedicated to another test tool that has been supercharging my (load) testing efforts for about 2 years now:

<center><a href="https://k6.io/"><b>k6</b></a>, an open source load testing tool.</center><br/>

> ***Disclaimer*** (same as for the [Postman post](https://filfreire.com/posts/frail_castiron_ep1)): this is not a tutorial. It's not a paid or endorsed review. It's a recollection of my experiences, feelings, frustrations and a flawed portrait of my user experience with the [k6](https://k6.io/) tool, from a software tester point of view. If I might sound negative at some points, I prefer to do so and stay true to myself as a tester, instead of making a blog post of shallow "praise and wonder". Read on!

## Setup

So, similar to [the other post](https://filfreire.com/posts/frail_castiron_ep1) let's start with a timeline, this post is about my personal experience using k6 from around mid-2019 until now (April 2021). I've used k6 with random consistency, sometimes multiple times a day, every day of the week on the most hardcore weeks, other times a handful of days per month between these timestamps, and I've used almost all of the k6 versions released between [`v0.24.0`](https://github.com/k6io/k6/releases/tag/v0.24.0) and [`v0.31.1`](https://github.com/k6io/k6/releases/tag/v0.31.1), the one I remember having the most interaction with being [`v0.26.0`](https://github.com/k6io/k6/releases/tag/v0.26.0).

I've used it on a lot of load testing efforts, and the most used "setup" was running load scenarios that were either "coded by hand" or generated through [postman-to-k6](https://github.com/k6io/postman-to-k6) library. The load scenarios could be anything from "*do these 2 API calls for a few thousand times*" to "*load these input data files from an S3 bucket into 50 load-generating k6 instances on a Kubernetes cluster to mimic this complex product flow of 500k users*".

I have __never__ used any [priced offering](https://k6.io/pricing/) of k6 nor have I ever used their [cloud](https://k6.io/cloud/), meaning that, even at scale, I've continued to use k6 from the free "self-hosted" perspective, and this post is always written considering only the free & open source user space.

Lately my interactions with the tool have not so much to do with reproducing huge scales of load, but two main topics: first, running a hands-off set of smaller load scenarios on a nightly basis and "spitting out" comparisons of each nightly load stats, and second, democratizing the access to load test tooling in the current organization I work with, where a non-technical person can, with a simple chat command trigger what is on its core a k6 instance running a user-mimicking load scenario (comprising a series of HTTP calls and receiving Websocket events), defining the Virtual users (VUs) and iterations in the chat command itself and getting back "human" meaningful results. At one point later in the year I expect to be back to the problem of large load tests/ distributed load generation, but I have other problems to solve in the meantime.

## What I liked 😀  / "The Honeymoon period"

To best describe what I like the most about [k6](https://k6.io/), let's start with a problem:

> I have very little time allocated for doing deep testing and even less time to invest in (equally deep and investigative) **Load** testing... due to *XYZ constraints*, so the time I do have available at my disposal as a tester/engineer, I need to use it to **quickly** sketch realistic **load flows** and then run a lot of experiments and investigate why the system under load works weirdly or breaks...

(*Pro-tip*: a system always does break or behave weirdly especially if it hasn't been tested (or thrown in production) at even the tiniest of scales, it's always like opening a can of worms, and it's always a good idea to load test.)

I had this problem and I needed to find a tool for it. And one day, by chance, a colleague ([Carlos](https://www.linkedin.com/in/carlosgimenoy/) you know who you are) whom I went to whenever I needed to know about either some arcane networking/infra piece of knowledge or about some specific tool that might help me solve some problem, turned up to me and said: *Hey Filipe, I think this would fit your load use-case, it's called [k6](https://k6.io/), I just tried it out on my machine, you should try it out too.*

I opened their page. Installed [k6](https://k6.io/) with a [brew](https://brew.sh/) command and tried out their example. And that was it, with an onboarding experience of "a few seconds", I started to get emotionally *convinced*.

I quickly searched if there was something that could help me port over in any way the product flows I had already defined as [Postman](https://www.postman.com/) collections quickly into k6, and there [was one](https://github.com/k6io/postman-to-k6). Then I looked around their documentation: it was straight to the point and had examples. No bullshit. None of that "*enterprise grade synergies to leverage power of closed-source load software for make benefit of big corporations*" bullshit. I was *hooked*.

I could specifically describe what I like the most about k6 in multiple topics:
- Ease of use
- Low barrier of entry/understanding
- Thinking in blocks

But instead I'll try to sum it all up in a single topic...

### Providing a great first user experience

One of the first things that hit me was the low (practically inexistant) "barrier of entry" to using [k6](https://k6.io/). It's straightforward to setup, and once installed, using the CLI (either [directly or with Docker](https://k6.io/docs/getting-started/running-k6/)) is as simple as using any other typical CLI tool that most technical folks might already be used to interact with every day.

Unlike most other common tools, which have:
- plenty of ways that you can "over-engineer" your load test scenarios, introducing a lot of different concepts that might seem foreign on first contact ([example](https://docs.locust.io/en/stable/writing-a-locustfile.html#)).
- plenty of CLI arguments, with the same kind of low-level abstraction to a single request ([example](https://httpd.apache.org/docs/2.4/programs/ab.html#options)) as a [curl](https://curl.se/) command;

k6 removes both these barriers by, in my opinion, assuming three simple principles:

- If given the choice, specifically when it comes to adopting new tooling, Testers and Engineers will avoid having to grasp new concepts, no matter the complexity (we are human, most of us are lazy, and most of us are busy);
- If you can present folks with a simple concept that they already know, they will do half of the work for you in terms of scaling that concept (e.g. how many of us think of building a vertical/horizontal "tower" the first time we play with a LEGO set);
- Don't indirectly force over-engineering for simple use-cases, if folks want to go deeper, let them explore which bits of functionality and documentation they want, without forcing them to learn different parts of the overall functionality and keep it in mind at all times.

By sitting on these concepts (either by chance or on purpose) k6 lets half of the magic work happen on the developer/tester's head:

- When I think of a a load scenario I don't need to learn anything new, I can start with something as simple as a "unit" check that I would naturally do to check if an API endpoint is OK-ish, or check if a series of endpoints that mimic a user flow appear to work sequentially, or a service with a Websocket responds some given event, ... - this is nothing new for anyone that tests the "function" of their APIs, the point being I'm not adapting my thought of testing an API to the tool, I'm going with "the flow" of how I already test an API;
- From the load scenario, if I want to think at scale, I think in terms that are easy to grasp from just trying them out:
```
A_Load_experiment = My_load_scenario * ( virtual_users And (iterations Or duration)
```
- If folks want to get into any topic, it's [contained and documented](https://k6.io/docs/).

The same principles apply when thinking of scale, from the local execution to large load tests:
- As a developer, I can run a load scenario against a local or hosted target service with a single command, the same way I would run `yarn run test` or `go run test ./...` to run a suite of unit/integrations checks on my codebase;
- If it's just a simple command and there's a [container for it](https://hub.docker.com/r/loadimpact/k6) - using it with any continuous integration/deployment software shouldn't be a blocker, and there shouldn't be any excuses for what was done as a one-time-only load experiment to not be easily reused and repurposed;
- If one k6 instance is doing the same load experiment that `N` k6 instances do at scale, then I can do the most intricate thing I want without being limited by any restrictions common of load vendors, or
- If I'm a beginner, I don't need to worry initially about distributed load generation concepts (e.g. having some sort setup with a "supervisor" and "runners"), I can with a rudimentary/simple setup extract benefits from running `N` k6 instances for the load experiment I'm trying to do.

Now that we've addressed my favorite parts, let's go into the next topic...

## What I didn't like 😠

### Version changes bringing surprises

I'm not sure if I can call this a point that I dislike, I guess it's not necessarily a fair overall point towards k6, but it was nevertheless a personal point of frustration, which I think other folks might have been affected likewise.

Long story short:

> *user of open source tool is dumb, doesn't read changelog, uses new version, new version has magic the user is not prepared for, breaking the user normal workflow*

Around the time k6 was updated from [`v0.26.0`](https://github.com/k6io/k6/releases/tag/v0.26.0) to [`v0.27.0`](https://github.com/k6io/k6/releases/tag/v0.27.0), there was a breaking change, that was by all accounts documented on [Breaking changes](https://github.com/k6io/k6/releases/tag/v0.27.0). It was a minimal change, and starts like this:

> Previously, if the iterations and vus script options were specified, but duration was not, the script could have ran practically indefinitely, given a sufficiently large number or length of the used iterations. (...) From k6 v0.27.0, by default, if the specified iterations haven't finished, these scripts will abort after 10 minutes (...) This default value can easily be changed (...) by setting the `duration` / `--duration` / `K6_DURATION` script option.

Now, first problem, right off the bat, as a *rascal* free open source user, I generally didn't read changelogs (lesson learned from that moment onward).

Second problem: an assumption was made, that most users' load scripts by default won't take more than 10 minutes. This is far from the truth for folks running k6 load scenarios at scales of 50k iterations, where each iteration will comprise anything between 10 to 30 different API calls.

Third problem: if the first idea that comes to the user mind isn't checking the tool's changelog, folks will inevitably waste time debugging and understanding: why on earth are their k6 load generator instances *dying* before they even have a chance to run for a while?

We found out the solution eventually, and the fix was literally a single line of code, defining `K6_DURATION` environment variable to a value that was more in line with the typical load experiment duration, but I believe, for this particular kind of breaking change, where an assumption is made towards the typical usage of the tool, it needs to be tackled differently, besides (only) documenting it in the changelog.

For instance, the whole trouble could've been avoided with a simple warning log when running the tool:

```
$ docker run -i loadimpact/k6 run - <script.js --vus 10 --iterations 1000

! DEPRECATION WARNING !: Hey you rascal, after v0.27.0
   whenever you use --iterations be aware that max duration defaults to 10min,
   no matter if you still have iterations to run.
   Read our changelog for v0.27.0 here.

          /\      |‾‾| /‾‾/   /‾‾/
     /\  /  \     |  |/  /   /  /
    /  \/    \    |     (   /   ‾‾\
   /          \   |  |\  \ |  (‾)  |
  / __________ \  |__| \__\ \_____/ .io

  execution: local
 (...)
```

This is a deeper problem than just the fact I didn't read changelogs and wasted time on something with a fix so simple. But we could discuss whether or not it would have been a valuable step to include some sort of deprecation warning in run-time for this kind of issue in particular.

We can consider it's indeed my fault as user for not being informed, but this is a tricky choice in the long run for winning over chunks of the community. On the contrary, assuming folks read the changelog, can lead to a lot of noise (see [this example](https://www.reddit.com/r/rust/comments/lfysy9/pythons_cryptography_package_introduced_build/), [and the same example on github](https://github.com/pyca/cryptography/issues/5771)).

This type of noise can, in my n00b opinion, be always prevented with either avoiding a breaking change, or what I personally think would be the more senseful choice, warning the user in run-time about any surprises.

### Memory and CPU fine-tuning

At one point we hit a lot of memory and CPU weirdness/issues for "containerised" k6 runners, especially true for scenarios that were intricate (with tons of requests and checks), where we would hit cases of load runners dying out-of-memory (OOM) even before being they were finished with the iterations.

When the issue wasn't dying with OOM, then it was the issue of the instances requiring a considerable amount of memory per pod that was running k6, e.g. 4 to 6 GB of RAM. It might not look much individually, but multiply that by 50 instances and we're talking about a small fortune in monthly EC2 bill... sure, the *rascal* in me will say, "well if it's the company paying and not me... *not my money*..." but we can all agree it's not an ideal situation.

As for the source and solution for those issues, it was always a point of fine-tuning, soul-searching and accurate guesses:
- We either had to tell k6 to [ignore "caching" responses](https://k6.io/docs/testing-guides/running-large-tests/#discardresponsebodies) of API requests, something which we only found out in the documentation long after we had burned through time and money on previous load runs... (yeah I know, we should have checked the documentation first...);
- The wonderful realization that "orchestrating" these k6 load pods through Kubernetes (k8s) doesn't mean we can magically scale infinitely in the *Age of Cloud*... we cannot have as many pods as we wish, if the cluster has limits... and clusters have limits, who would've guessed it, right?
- We disabled at one point lot of assertions/checks in some load flows [following also what the docs recommended](https://k6.io/docs/testing-guides/running-large-tests/);
- We had to "code by hand" a way to stop an iteration on the first failure, to free up the VU to start another iteration. This was specific to a flow we wanted each VU to stop trying to send requests for stuff that happened after a failed check. There were [some ways](https://k6.io/docs/using-k6/thresholds#aborting-a-test-when-a-threshold-is-crossed) to so something similar to this, but we found out that if a part of the flow was failing, even if we [failed the check](https://k6.io/docs/using-k6/thresholds#failing-a-load-test-using-checks), k6 would still try to run the other requests in the sequence for that VU.
- ...

Figuring out each of these issues meant that, we **eventually** knew implicitly that if a single load generating pod in k8s had "*this much CPU and this much memory*", it could hold these many VUs running this particular complex load scenario, and if something was dead or buggy, our test would fail sooner, but there was a lot of trial and error and experimenting to figure all of that stuff out.

Note, this "dislike" point isn't new for anyone that has had to do deep load test experiments regardless of the tool choice being k6 or another tool. One point of praise is that at least k6 makes the attempt to [document their benchmarks](https://k6.io/docs/testing-guides/running-large-tests/#benchmarking-k6-on-aws) for folks to reproduce or guide their own setups while most other tool providers provide benchmarks that are of "used toilet-paper" grade.

### Pain-points of having to use "large" data files as input

One of the indirect reasons memory was a problem was the issue of using large input data files. We had hit a limitation at one point where we wanted to make sure that for each iteration of each virtual users, a unique line from an input data file was being used. This was tricky for two main reasons:

- The size of the file could clog the load instance spin-up time (something which [also happened for other folks](https://community.k6.io/t/long-setup-times-when-implementing-unique-vus/726)), or result [in OOM errors](https://community.k6.io/t/out-of-memory-with-more-virtual-users/333);
- We had data collision issues during runtime and we definitely [weren't the only ones crossing this issue](https://community.k6.io/t/when-parameterizing-data-how-do-i-not-use-the-same-data-more-than-once-in-a-test/42);

I was no stranger to these, especially in moments where it was required to do specific product flows for about half-million test/staging users. These users existed in some form on a target database, so no user-creation was needed for some flows, and the input data files were sitting on some S3 bucket ready to be downloaded and "put to work", BUT the issue remained, with flows that required reading data from input files we'd always have to tackle the above issues.

If the files were too big (*past a magic number*), the k6 instances became clogged and wouldn't "boot" due to having to hold "a lot" of data in-memory. So we split those files and created different "collections" of the same dataset, and 500k users would be chunked into several files, depending on numbers of k6 instances we wanted to spin up. It was quite common to see: "*let's use the 5000-per-chunk collection today... which we can use to feed these many k6 instances, or the 25000-per-chunk collection today...*".

After that, we had to guarantee that every user on that data file was only attempted once, which meant we'd have to do a trick ([similar to this one](https://community.k6.io/t/when-parameterizing-data-how-do-i-not-use-the-same-data-more-than-once-in-a-test/42/2)) with how we loaded the data file and how each virtual users in a load run would get a unique "cross-section" of data to use for iterations. Even with an adaptation of the above trick, we hit collisions where near the end of a load run, a handful of virtual-users would try to re-use data that had already been used, causing a few "false" failures.

> Note: it seems this issue has been recently "officially" solved on [v0.30.0](https://github.com/k6io/k6/releases/tag/v0.30.0) (see this [Github ticket](https://github.com/k6io/k6/issues/532) and [this pull-request](https://github.com/k6io/k6/pull/1739)). Haven't tried it yet, but it's promising.

## Mixed feelings 😕

### Solving the distributed load generation problem for tight budgets

Solving the distributed load generation problem ("*how do I make it so my test runs on multiple load generating instances in a seamless and coordinated way, and see a sum of all results afterwards?*") was (and still is) very much a gruesome problem for open source users. Note, it's not a [brand new problem](https://github.com/k6io/k6/issues/140) and has been [acknowledged by folks that develop k6](https://k6.io/docs/testing-guides/running-large-tests/#distributed-execution).

k6 supposedly provides better support for large load tests in its paid SaaS cloud offer... BUT, there's a catch, unless the Engineers in the project have "access to the credit card" in the organization, or can convince the right folks, trying out or even thinking of using the paid options is already for many a rejected option. The bigger and more structured the corporate environment the worse it becomes to convince someone "above" that one's team needs access to something like a k6 cloud paid subscription. Oftentimes the context is: there are already folks in the corporation that have sold their souls to other load tool brands and it becomes a pointless pursuit bordering on the domain of internal political and organizational power-balance battles which few people are naive or unsuspecting enough to pursue.

This means that distributing load ultimately becomes a problem that falls into the Testers/ Engineer lap, and they will have a brand new set of different problems to deal with:

- Containerizing the tests (e.g. with k6 container + the coded scenarios);
- Mounting (and splitting) any test data files e.g. text files with a pool of users for login with the container;
- Where to host the containers and how to "orchestrate" them;
- How to monitor both the load generation containers execution and target-of-load systems;
- How to save reports/results/stats for later analysis;
- How to easily kill the distributed load generators in an emergency (e.g. killing infrastructure for everyone, so we need to stop the tests);
- Merging multiple reports data that come from different load generation instances;
- Making those reports/results meaningful to humans;
- All those points PLUS the fact the Engineer will likely need to configure the target-of-load system, either by spinning up the number of target instances, spinning up resources for any caching or persistence instances, ...
- ...

For a lot of these problems, you either have the luck of managing through a "tech miracle" to solve them, or you have the luck of being given the time and resources to solve them, or your team has already solved some of them for other use-cases, or you have a bright high-IQ extremely underpaid intern helping you out, freeing time for you to focus on doing plenty of actual load experiments. Otherwise, as the user you'll be in muddy waters.

<small><i>(don't worry Billy, that promotion is coming, we know you are contributing more for this company than most C-levels, but we just believe you're not quite there yet...)</i></small>

To give a practical example, let's use the point: ***How to monitor both the load generation containers execution and target-of-load systems***.

The fact that k6 leaves this bit to the user (which is understandable, it shouldn't try to do everything) becomes another point that might make or break load testing efforts:

- You either setup everything from the start so you have observability into what is happening on the load generators (and the targets) themselves, for example by posting the load generation logs to log aggregators, and the load container details (cpu, memory, processes, ...) to observability software (e.g. [Honeycomb.io](https://www.honeycomb.io/), [Datadog](https://www.datadoghq.com/), [Instana](https://www.instana.com/)...);
- Or, if you have no log aggregation/observability setup (and some tech orgs are still in this state 😬) you'll resource to the basic method of *SSH'ing* into a load generation container and `tail` k6 logs in order to figure out what is happening, or running `top` to check what processes are doing in terms of CPU/Memory...
- Or you are left guessing (and potentially give up, like most do).

Self-hosted life means dealing with this kind of stuff. Is this a positive or negative thing? The answer is: Yes.

### postman-to-k6 converter needs some love

To talk about [postman-to-k6](https://github.com/k6io/postman-to-k6) could be a post by itself. I'll try to keep it brief: [postman-to-k6](https://github.com/k6io/postman-to-k6) needed (and likely still needs) a lot of love. It's a wonderful tool to work with for simple collections, like when you are trying to do some simple exploit, so the collection is just a handful of simple API requests, BUT, it's awful for postman "power-users" that have to work with intricate setups.

Now, to be fair this is not the fault of [postman-to-k6](https://github.com/k6io/postman-to-k6) alone. The fact is, in this case we are talking about creating and maintaining complex postman scripts that already reach [limitations in performance of the postman client](https://filfreire.com/posts/frail_castiron_ep1) itself. From the perspective of the converter this means we're talking about trying to convert collections that:

- Have tons of custom functions on the [pre-request](https://learning.postman.com/docs/writing-scripts/pre-request-scripts/)/[test](https://learning.postman.com/docs/writing-scripts/test-scripts/) stages;
- Has a lot of ugly duct-tape code specifically coded to solve specific problems;
- And that makes use of the different [environment/variable scope levels](https://learning.postman.com/docs/sending-requests/variables/#variable-scopes) that exist in postman in order to maintain test state/variables at different scopes;

These are conditions that I assume the [converter](https://github.com/k6io/postman-to-k6) was never designed to tackle, but I was hopeful in the beginning it would. When I reached this problem, it meant the extra-work of creating dumbed/stripped down versions of particular scenarios in Postman, with a lot of hardcoded stuff in them, and only then convert them back to a k6 script. And even then it meant at times, debugging compatibility issues between different k6 versions that surfaced on some of the [libs](https://github.com/k6io/postman-to-k6/tree/master/lib/shim) that the [converter](https://github.com/k6io/postman-to-k6) would pre-include on a converted script, or investing time adapting generated code (when doing a "vanilla" k6 script would have meant investing less time).

There's more to be said about this, in k6's case, my work-around recommendation is, if possible, avoiding converted scenarios, and starting from scratch as much as possible.

## What I hope for the future 🌱

I've written a [parody](https://filfreire.com/posts/how_to_get_rich_fast) in the past about *doing business* in load testing, sort of as a critic to a lot of foul play I observed from some load testing vendors through time. Generally the options for load testing tool choice are:

- Either typical *enterprise* stuff that is oftentimes accepted (gently imposed) in corporate environments or
- "old but gold" & open source stuff (like [this](https://httpd.apache.org/docs/2.4/programs/ab.html), and [this](https://jmeter.apache.org/) or [even this](https://www.joedog.org/siege-home/)).

Both paths have their pros and cons, but both generally suffer from the same evil: the tool is not easy for a *n00b millenial* (like me) to "*pick up and play*"... and I don't even want to think of what Gen Z will say about this at one point in the future.

In this context, I personally think [k6](https://k6.io/) appears in a third rare group: tools that try to solve a problem that has already been solved by many, but democratizing the access to the solution to everyone, no matter their previous knowledge on the topic of the tool. And this can mean a lot of things: being open source first, no (hidden) limits for "free"-tier users, straight to point meaningful documentation, reliable and natural onboarding experience, adaptability of the tool for any kind of use- be it simple one-time-only use or continued and hardcore use, ... in most of these things tools like [k6](https://k6.io/) with its strengths and limitations: **delights**.

With that said, I leave for the folks that develop [k6](https://k6.io/) a few wishes/hopes for the future:

- Share more examples for distributed load generation setups with nitty gritty details: e.g. you're new to distributed load problem? Here is what the problem is, and here is what you can do on your own on AWS or other providers for spinning up multiple load generators running your scenario, and yes, you can always mention: *and if you pay us instead, you get all this stuff "for free"!*

- Similar to the above point, I think publishing more benchmarks would be beneficial for users. [k6 does provide some example benchmarks](https://k6.io/docs/testing-guides/running-large-tests/#benchmarking-k6-on-aws), and it does one thing a lot of tool vendors don't do, they don't just post the results of the benchmark, they also post details on how you can reproduce it on its own, which is already miles ahead of many tool providers, but I see more benefit in trying to reach out to the community and figuring out new intricate benchmarks that might be worth publishing that folks can equally reproduce. I understand this would be tricky most stuff that the community does is closed-source (including most of what I've done in the past or do presently), but I'm sure something can be done.

- Aggregation of distributed load test results is a problem that should have already been solved (and open sourced) and not left for each self-hosted user of [k6](https://k6.io/) (or any other load tool) to have to invest time solving again; We can say, sure it's already solved if users "*do this and that, ?????, profit your load test reports/results have been merged!*", so it's not impossible, but there's still tons of opportunity for it be provided as a simpler open source out-of-the-box solution for folks who aren't tech-savvy. I can't even begin imagine what the community will do once they are supercharged with this.

- Open source is the way to go, continue doing this. I wish the market will get over time more examples like [k6](https://k6.io/): open and enabling of anyone to pick up and use, no trials,  no "licenses", no register your email for interest so one of our trained intern salespeople can sell you crap...  There's still "too many" corporations siphoning money into closed-source load generation tool vendors, selling their souls, doing blood-pacts with key folks inside organizations, and folks get hogwash load generation solutions promoted as "default" for their organization, ultimately wasting a lot of money for long 5-year / 10-year cycles.

- Provide tooling to abstract "this stuff" to make it available for non technical users (be them dedicated testers or product people), think [netlify](https://www.netlify.com/) or [vercel](https://vercel.com/), but for load testing, where nitty-gritty "boring" details that every org "gets stuck on/reinvents the wheel" are already neatly solved, leaving folks more time to experiment and do "the thing". I assume I'm mentioning this point because, in all honesty, I've never tried [k6 cloud offering](https://k6.io/cloud/), which likely is the attempt to do exactly this. Such is life.


________

_If you read this far, thank you. Feel free to reach out to me with comments, ideas, grammar errors, and suggestions via any of my social media. Until next time, stay safe, take care! If you are up for it, you can also <a href="https://www.buymeacoffee.com/filipefreire">buy me a coffee ☕</a>_