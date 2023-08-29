---
layout: post
title: "Diffusing More Objects"
date: 2023-09-25 07:00:00 -0000
categories: diffusion model object detection
excerpt_separator: <!--more-->
---

Diffusion models are a popular family of neural networks for generative AI. 
They can generate new samples such as images. 
Recently, researchers explore whether other types of outputs can be generated. 
For instance, object detections: bounding boxes with a class label and confidence score. 

<img src="https://gertjanburghouts.github.io/pictures/diffuse_more_objects.jpg">

Diffusion models are stochastic by nature, because each output is a different generation. 
We have leveraged the stochasticity to retry the generation of object predictions for hard cases, 
such as small objects or low-contrast image regions. 
This idea works, as you can see in the image above: more objects are detected. 
