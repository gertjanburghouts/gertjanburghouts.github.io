---
layout: post
title: "Efficient Transfer for Objects using Diffusion"
date: 2023-10-28 09:00:00 -0000
categories: diffusion models object detection
excerpt_separator: <!--more-->
---

Our paper was accepted at the NeurIPS workshop on Diffusion Models! 
It's about efficient domain transfer, using semi-supervised learning. 
A model was trained on frontal images from MS-COCO, but we want to apply it to drone images that look very different. 
The objects are much smaller and the viewpoint is very different. 

<img src="https://gertjanburghouts.github.io/pictures/diffusion_method_2023.png">

First, we improve the recall of the method, by accumulating detections. 
Next, we use the improved detections as pseudo-labels for the unlabeled images, combined with 10 labeled images, in a semi-supervised setup. 

The performance can be improved, as shown below, from left (original model), middle (improved recall) to right (semi-supervised learning).

<img src="https://gertjanburghouts.github.io/pictures/diffusion_result_2023.png">

See Publications for more information.
