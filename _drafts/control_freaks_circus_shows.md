---
layout: post
title: "Control freaks and Circus shows"
meta_description: "Control freaks and Circus shows"
date: 2019-05-22
categories: [testing, personal experience]
image: /assets/images/2019/07/shooter.jpg
caption: "Shooter, 2007"
---

Nowadays the software industry is plagued with a set of very interesting (or nasty) problems:

- "Agile" can be about anything, specially about being "FAST" (when it is convenient), as oposed to, originally, a set of principles and ideas defined by some dudes in a manifesto for the ("low-level") tasks of software development (aka. coding);
- The need to quantify things which are not really fully quantifiable in numbers, for example, the old "*Quality (Patent Pending)*" (by craftsman testers defined as a value relationship of something with someone, and in the "Agile" world defined as a contraption of understandings of "some stuff of something, blah blah blah, can you QA this?");
- That "Agile Scrum Delivery Product Owner Managers Inc.", while being paid for the most part for the single responsibility to decide release timelines based on the information they should hold at any time of "what are the risks", "what seems to be ready", "what might we be missing", etc., relay that single responsiblity of "release decision" to Testers or to "QAs";
- Complete perversion the role of a Tester, which is to hunt down for the information mentioned before, and not to act as a magical "gatekeeper of bugs";
- Complete perversion of the role of someone responsible for quality assurance, which is, for the most part, to define multiple "keep everyone accountable/in check" processes, and not to act as a magical "assurer of quality";

All of these nasty problems often translate into sometimes we as Testers getting distracted: we're eager to accept the results of automated checks (which are not a replacement for meaningful testing), we trust the results, code gets merged, only for us to minutes/hours later realised: it would have been a better idea to run some experiments and test properly some parts that the automated checks will never complain about. And we find ourselves in situations where we missed very apparent bugs had we taken a mindful perspective instead.

The same applies when Testers share abstract (and not very meaningful) results with folks in delivery/management positions, for example, about number of test cases passed, or number of portions of work that have been tested. The delivery folks are often in a rush, uphold any of these non meaningful numbers as a global truth and the Testers fail to pass the most crucial message:
> "Guys, these numbers don't mean anything, in fact, we've been thinking, and these test cases only scratch the overall surface of what we have to test, we would like to test more deeply these specific experiment cases..."

I've seen this happening time and time again: based on people's observations, beliefs are built that something is ready, because the Testers have been "seemingly" testing for quite a while, when in reality the build they need to test or the environment is not ready. The truth is that a big time interval could have been spent doing other stuff while waiting for a build, or retesting and stumbling on issues which don't allow one to cover more of the whole system they need to test.

How to avoid this kind of stumble: testers own your stuff (to avoid saying a curse word).

Own it to a point you can tell your *"Agile Scrum Delivery Product Owner Managers Inc."* to kindly take a hike when that person asks you to martyr-like own up to release decisions.

The sooner you as a tester own the risk, bug and problem information flow, and own the representation of that information, the better. Otherwise you'll lose yourself in a train of rushedness (which is normal in nowadays software projects), silly or obscure expectation management, and you'll have someone who doesn't know anything about testing, gently wispering to your ear, telling you how to convey evidence of your own work.