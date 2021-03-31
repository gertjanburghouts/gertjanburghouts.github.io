---
layout: post
title: "Learnable detection of moving objects"
date: 2021-03-31 23:00:00 -0000
categories: moving object detection
excerpt_separator: <!--more-->
---

When objects appear very small in images, standard object detection has difficulties. 
This is because it relies on the object's texture, which becomes invisible at such small scales.
Detecting small objects based on their motion is a better alternative. 
See the image below, where a standard detector fails (top row) and a motion-based detector (bottom row) detects the small objects.

<img src="https://gertjanburghouts.github.io/pictures/moving_object_detection.png">

<!--more-->

The motion is captured through the second and third channel of the image, 
by a so-called difference image which identifies changes across consecutive video frames. 
The first channel contains the gray image. 
That is why the images in the bottom row look a bit weird: they are a combination of shape and motion. 
These image representations lead to better detection results, see the performance graph below. 
Where standard object detection fails for small objects (towards the right), the motion-based detector performs much better.  

<img src="https://gertjanburghouts.github.io/pictures/mod_roc.png">
