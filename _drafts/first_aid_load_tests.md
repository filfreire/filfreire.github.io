---
layout: post
title: "A first-aid in load testing"
meta_description: "A first-aid in load testing"
date: 2020-07-31
categories: [testing, load test, load generation]
image: /assets/images/2019/05/deltaforce.jpg
caption: "Delta Force, 1986"
---

## Lose the fear

todo: "it looks hard, but it isn't that hard"

## Understand minimally what you are trying to do

todo: concept of a target system, a load you want to try, and what things do you want to check - normal scenarios, scaling scenarios, chaos scenarios, "throughput based on iron" scenarios, and so much more.

## Getting technical

### Define a load flow (E.g. Postman)

todo: explain how to quickly define a simple load flow, that fetches data from csv, uses it in one request, and then we reuse request's data on a later request.

### Convert it to a load script (E.g loadimpact/postman-to-k6)

todo: explain how to convert the exported postman collection, and adapt and improve the load script that is generated by default

### Test it out on your machine

todo: test out on your machine, and try to get a hold of some important concepts: iterations, virtual users, error handling, logging, scripts that will make your life easier

### Interpreting measurements

todo: talk a bit about what you can measure that is provided by the load tool; and what you should look for in the target system

## What's next?

In next post we'll look a bit better into possible load generation structures, where you can define a specific setup of how to host multiple load generators, and tackle fetching different chunks of test data to be used in the load tests
(put an example screenshot of setup of my postman talk)

