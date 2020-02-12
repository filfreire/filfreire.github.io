---
layout: post
title: "Rapid Prototyping of Load Tests"
meta_description: "Rapid Prototyping of Load Tests"
date: 2019-05-22
categories: [tools, testing, api testing, postman, personal experience]
image: /assets/images/2019/05/deltaforce.jpg
caption: "Delta Force, 1986"
---

1) figure out the test flow and what you want to measure
2) write down a single user flow on postman
3) export the postman collection and convert it to a load script (postman-to-k6)
4) try out the load script with k6.io
5) bootstrap a proper load generation setup (ec2 flavor and k8s flavor)
6) deal with test data in concurrency scenarios (k6.io big limitation

