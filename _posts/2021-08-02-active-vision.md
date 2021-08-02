---
layout: post
title: "Active Vision for Robotics"
date: 2021-08-02 18:00:00 -0000
categories: active perception robotics
excerpt_separator: <!--more-->
---

The cool thing about a robot is that it can act to improve its performance. 
For instance, by getting closer to the object, more details can be perceived, thereby resolving uncertainty. 
This demo video shows that the robot successfully approaches and confirms the objects of interest, and quickly abandons the other irrelevant objects.

The robot’s goal is to find human dolls. Sometimes the object is not a doll, but a transformer toy. 
At first, it is always uncertain, because the object is very small. It decides to get closer to resolve the uncertainty. 
More detail is helpful to resolve what the object is.

<iframe width="437" height="248" src="https://www.youtube.com/embed/2F7tMYG50J8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--more-->

The idea is that the robot stops getting closer, once it is certain. 
Otherwise valuable time is wasted by getting very close to every object that the robot encounters. 
It stops getting closer when a large decrease of confidence is observed for the object(s) of interest. 
In that case, it has become confident that it is some other irrelevant object.
