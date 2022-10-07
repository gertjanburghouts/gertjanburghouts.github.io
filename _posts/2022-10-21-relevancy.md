---
layout: post
title: "Unknown but Relevant?"
date: 2022-10-21 09:00:00 -0000
categories: outlier anomaly relevancy
excerpt_separator: <!--more-->
---

Consider a robot operating in an open world, which sees novel classes during deployment. 
Or a police analyst who inspects a hard drive of photos and does not know beforehand what can be seen on them. 
Often, the user has a particular interest, e.g., vehicles. 

But, the user may not know all possible types of vehicles beforehand, or, there are not yet images of them. 
There are common techniques to separate the novel classes from the known classes. 
We address the problem of further dividing the novel classes into relevant versus irrelevant novel classes. 

<img src="https://gertjanburghouts.github.io/pictures/known-unknown-relevancy.jpg">

For instance, the user who is interested in vehicles, has images of buses and shows these to the model, 
and wants to be informed when an image contains another vehicle type, while ignoring the non-vehicle objects. 
Our model will group various test images into known (buses), unknown relevant (vehicles) and unknown irrelevant (non-vehicles), see the figure below.
