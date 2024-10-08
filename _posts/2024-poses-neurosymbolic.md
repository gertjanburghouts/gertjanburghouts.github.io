---
layout: post
title: "Zero-shot neuro-symbolic body parsing"
date: 2024-10-06 06:00:00 -0000
categories: pose estimation classification neurosymbolic AI
excerpt_separator: <!--more-->
---

To interpret human behaviour from a single image, a cue is provided by the body pose. 
However, for rare behaviours, not many training images are available, sometimes none. 
We approach the problem in a zero-shot manner, without any training images. 
We formulate logical patterns of body keypoints, which are interpreted by neurosymbolic AI. 

In the first example, generally the arms are stretched out before the body and both hands hold the object. 
Therefore, we define that the two hands, elbows, and shoulders are at roughly the same height and both hands are close to each other. 
In the second example, the hands and shoulders are at roughly similar height, however the two elbows are not. 

<img src="https://gertjanburghouts.github.io/pictures/poses.jpg">

Presented at SPIE 2024.
