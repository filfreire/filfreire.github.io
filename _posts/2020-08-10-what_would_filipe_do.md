---
layout: post
title: What would Filipe do?
meta_description: "What would Filipe do?"
date: 2020-08-10
categories: [testing, raid software testing, guerrilla testing]
image: /assets/images/2020/08/truman.jpg
image_alt: a movie still from The Truman Show from 1998
caption: "The Truman Show, 1998"
---

Nearing a moment of change in jobs, a few people asked me if I could lay out a short draft of "_what would Filipe do_", that could serve as a source of guidance/inspiration for a near future where I'm no longer a part of the team's picture. I realize that this in itself is tricky, because the moment someone leaves a team, the team is no longer the same, becoming a different team, with new unknown dynamics and fading past implicit relations or context. 

Still, I was able to make a rough sketch of what I believe might help, taking into account the context of the main project I worked in, that has been always marked by:
- on one end the guerrilla efforts of a tight-knit team, focused on delivering value, while mostly going against the default organizational design, breaking apart supersticious standards and beliefs;
- on the other end, having to deal with complexity and limitations of different services, while working long hours under hardcore pressure, high expectations, and high risk.

From a Testing perspective, it ended up being an _impromptu_ testbed for my own methodology, [Raid Software Testing](https://raid-software-testing.com/), still in its infancy.

What follows is a set of guiding principles that have helped me and my colleagues, in no particular order:

## Don't focus on numerology

We oftentimes might fall under the seduction of attempting to put Testing, or the evidence of Testing, into a pretty box for the sake of doing something similar to a "circus show". We start by trying to impose preconceived values without having a look at the context and tempos of the project.

Imposed values quickly evolve to a focus on wrongful metrics, without doing much valuable and meaningful Testing work. My advice is: before focussing on gathering any numbers or percentages or filling out coverage sheets, try to get a potent grasp of your surrounding context. If you or your testing team are not the most valuable players when it comes to finding critical, risky, and meaningful bugs, and instead it's someone from Senior Management or external malicious users finding those bugs first, they're closer to "_the truth_".

To put in perspective: One of the reasons bot developers in the sneaker reselling scene are oftentimes many steps ahead of their targets is precisely because the time the targets are wasting not doing deep testing (say, by coming up with numbers and percentage _fan-fiction_, to seduce themselves with illusions of control), is the same time bot developers are investing doing some of the deepest and unconstrained testing most professional Testers, sadly, only rarely can afford to do. 

## You always need a dedicated Tester

When a decent Tester leaves a team "_Tester-less_", some folks might entertain the idea that they don't need to replace that Tester, or that the "Developers can Test" (assuming the Devs themselves don't follow the Tester's footsteps and abandon ship... bold assumption, I know). Here's a problem with this idea: it's stupid.

Companies/projects that have decided to at one point discard completely the need for any meaningful Testing, see an increase in embarrassing bugs that would have been caught by skilled testers.

This increase is then linked with a familiar contemporary problem of users tolerating a growing number of embarrassing bugs and crappy function, with the usual symptoms:

> _"We did an oopsie!" "Our monkeys will fix this quick!" "Something is wrong!" "Ups, we may have inadvertently lost/sold your data to evil entities!" "Sorry, not sorry, we may have influenced your family into becoming a tiny bit more racist and ignorant"..._

The above happens in parallel with tremendous feats of "_smoke-selling_", with some of these companies going as far as writing books "about Testing" or tech blog posts showing "the future of Testing"... The same companies that dubiously dance around ethical issues, exploit users, kill off functioning products and make their own products crappier through time.  _\*Cognitive dissonance intensifies\*_

The advice here is: **invest in skilled software testing** and don't entertain the idea of testing as a low skilled "button pushing" activity: you need someone who is articulate about Testing on your side.

## Always go deeper

When we're Testing or thinking about Testing ideas, we don’t go deep enough. When we try to go deep, we’re not nimble or on the lookout for wormholes/distractions, and we waste time going “_fake deep_”, like doing the same incoherent thing over and over again expecting sudden enlightenment (it might happen but it just so happens we actually need to go deeper in those cases).

We glue ourselves to the timing and the tempos that are documented or defined where we can only see a system through an “_expected interaction and response flow_”, and we don’t try and mess with the actual interactions of the services or state-machines we're testing. This is one of the things "malicious" users of our software end up doing (and exploiting) in an unconstrained and smart manner. For them nothing is forbidden, their minds are free.

We uphold, sometimes in a fanatic way, expectations for "_immutable truths_". If it's described in the ticket, we do it, but we never dare to step outside of the confines of "_the expected_", and think about the unexpected messy parts. This ends up being the road most traveled, and few deviate from it. This points to, what I believe, is a characteristic of competent Testers: by the time they put a step on said road, they have already charted the surrounding terrain, hidden roads, and brought up some explosives for some special occasions... "_just to feel something._"

## Be nimble and resourceful about tools and learning

Tools are just tools. Don’t be blinded by promises of coverage breadth, or even depth. 

To avoid wasting time fantasizing about tools, keep focused on what matters:
- Ask yourself "are there important bugs in my product"? 
- What do I need to have in terms of scripts or automated checks to help signal the above bugs?
- What tools would help me debug, investigate, monitor, and trace issues in production and test environments?
- What low (and high) hanging fruit is out there in terms of increasing the testability of my project?
- ...

If you're in the business of hiring Testers, do your future self a favor, and bear in mind that, even if they’re certified, it's often the case that certification itself is "paper-thin", or equivalent to memorizing 4 sheets of paper and then doing a quiz. Instead, provide ways for your Testers to do proper testing training. Here are two personal recommendations: [Rapid Software Testing (RST)](https://rapid-software-testing.com/) and [Black Box Software Testing (BBST)](https://associationforsoftwaretesting.org/bbst-black-box-software-testing-courses/).