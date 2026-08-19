---
layout: post
title: "Teaching Robots Where to Go: One World, Many Bodies"
date: 2026-04-08 06:00:00 -0000
categories: occlusion camouflage partial visibility
excerpt_separator: <!--more-->
---

For humans, deciding where a robot can drive or walk seems easy: the path is traversable, the tree is not. 
For robots, it is much more complicated—and it depends on which robot you are talking about. 
A SPOT can step over obstacles that would stop a TurtleBot, while an Atlas or a Roomba has yet another set of capabilities. 

We therefore developed a traversability system that explicitly takes the robot’s embodiment into account. 
Before deployment, an LLM reasons about the robot’s morphology and capabilities and translates this into relevant concepts for perception: 
what surfaces can it handle, what objects are obstacles, and what situations require caution.

<img src="https://gertjanburghouts.github.io/pictures/traversability_3.jpg">

We then combine three complementary foundation models. YOLO-E provides fast, open-vocabulary object detection, 
while SAM3 turns relevant concepts into precise pixel-level segmentation. 
A VLM adds an open-world safety net: when the scene contains something that was not anticipated by the prior knowledge—say, 
a cardboard box suddenly blocking the road—it can reason about its meaning and enrich the traversability analysis. 
The result is a robot-specific map of the scene, where green means “go ahead” and red means “better not”.

<img src="https://gertjanburghouts.github.io/pictures/traversability_2.jpg">

The interesting part is that there is no single “correct” traversability map. 
Traversability is a relationship between the world and the robot. 
The same staircase, branch, puddle or box can be perfectly manageable for one robot and a hard obstacle for another. 
By combining LLM reasoning, open-vocabulary perception, segmentation and VLM-based open-world reasoning, 
we are moving from robots that merely see their environment toward robots that understand what that environment means for them.

<img src="https://gertjanburghouts.github.io/pictures/traversability_4.jpg">

