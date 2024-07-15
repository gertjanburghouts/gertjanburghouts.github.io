---
layout: post
title: "Scaling 3D Reasoning"
date: 2024-07-15 06:00:00 -0000
categories: large multimodal models reasoning environments robotics
excerpt_separator: <!--more-->
---

Large multimodal models (LMMs) are useful for many robotics capabilities, including spatial reasoning and semantic scene understanding. 
However, they do not scale well to large environments. 

We decompose the environment into smaller rooms. 
Each room is a node in a graph. 
Scalability is achieved by expanding the graph to new rooms iteratively. 

Connected rooms are representated by relations in the graph. 
Various routes become apparent in this way. 

Given the objects found in the rooms, the robot can reason about the safest route. 

<img src="https://gertjanburghouts.github.io/pictures/rss_poster.jpg">

Accepted at the Robotics: Science and Systems, Semantics for Robotics, 2024.
