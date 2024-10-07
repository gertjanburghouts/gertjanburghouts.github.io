---
layout: post
title: "Zero-shot neuro-symbolic body parsing"
date: 2024-10-07 06:00:00 -0000
categories: pose estimation classification neurosymbolic AI
excerpt_separator: <!--more-->
---

To interpret human behaviour from a single image, a cue is provided by the body pose. 
However, for rare behaviours, such as aiming a weapon, not many training images are available, sometimes none. 
We approach the problem in a zero-shot manner, without any training images. 

We formulate logical patterns of body keypoints, which are interpreted by neurosymbolic AI. 
Aiming a handgun is different from aiming a rifle. 
When aiming a handgun, generally the arms are stretched out before the body and both hands hold the gun. 
Therefore, we define that the two hands, elbows, and shoulders are at roughly the same height and both hands are close to each other. 
Aiming a rifle is defined by the hands and shoulders at similar height, however the two elbows are not. 

<img src="https://gertjanburghouts.github.io/pictures/poses.jpg">

Presented at SPIE 2024.
