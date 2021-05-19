---
layout: post
title: "Learning from Simulation and Games"
date: 2021-05-19 10:00:00 -0000
categories: object detection synthetic data
excerpt_separator: <!--more-->
---

Sometimes images of objects-of-interest are not available. 
For instance, rare objects such as a tank. 
Can we train an object detection model on simulated images? 
Yes, we can! 
A model trained on the game GTA-5 detected these objects in YouTube footage. 

<img src="https://gertjanburghouts.github.io/pictures/gta-detector.jpg">

<!--more-->

The game GTA-5 was used to create synthetic images. 
The images look very photo-realistic. 
We changed viewpoints, viewing distances, and various weathers - to learn a model that's robust to changing conditions.

Research was funded by the V1508 program and NATO RTG-144.
