---
layout: post
title: "Zero-shot Object Localization"
date: 2021-06-22 09:00:00 -0000
categories: zero-shot learning object detection
excerpt_separator: <!--more-->
---

Detecting objects is important and works very well. 
But, to learn a model, many images are required. 
We research techniques to learn with less labeled images. 
To the extreme: zero labels.

<img src="https://gertjanburghouts.github.io/pictures/zero-localization.jpg">

Our approach is to learn the object by its known parts. 
For instance, a bicycle composed of a frame, saddle, steer and wheels. 

Because there can be multiple bicycles in the scene, the algorithm needs to reason about the parts and their possible compositions. 
To that end, we developed a multiple hypotheses method that takes into account multiple criteria about parts, such as their overlaps and relative size. 

<!--more-->

Published at AAAI-MAKE 2021: "Detect objects without training examples, by knowing their parts".
This conference's topic is Combining Machine Learning and Knowledge Engineering. 
Very relevant for the latest developments in Hybrid AI.

This work was sponsored by RVO Challenge (2020) and RVO Disruptive Sensors (2021).
