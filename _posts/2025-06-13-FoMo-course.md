---
layout: post
title: "Lecture on Foundation Models"
date: 2025-06-13 08:00:00 -0000
categories: foundation models university lecture
excerpt_separator: <!--more-->
---

Every week, a new large AI model is released by the big tech companies and research labs: 
CLIP, Flamingo, Grounding DINO, SAM-2, etc. 
They offer a big potential for us, across a broad range of capabilities. 
From image classification and retrieval (CLIP) to object detection (Grounding DINO), 
scene segmentation (SAM) and Visual Question Answering (e.g. GPT4o). 

The question is how to use them optimally for the task at hand. 
One challenge is that today’s large AI models are trained on everyday web images with common objects 
(cars, skateboards, types of cats, etc.). 
Clients often want something different: other images (e.g. drones that have other viewpoints) 
and/or other objects. 
It requires some tricks to adopt large AI models for our capabilities, we call these adoption strategies. 

We have identified four strategies:
(1)	include pre- or post-processing, e.g. to apply the model to pre-filtered image regions, or to check or clean-up the predictions afterwards. 
(2)	change the model behavior from outside, by changing the textual prompt, or improve the question.
(3)	re-learn part of the model, by adding a few learnable elements (e.g. prompt tuning, LoRa), or finetuning all weights (e.g. few-shot learning). 
(4)	change the model itself, i.e. its architecture, for example to modify the tokenizer which enables to learn without forgetting (e.g. Grounding DINO extension that it can learn new objects without forgetting known objects). 

During this lecture, I have discussed these four strategies. 

<img src="https://gertjanburghouts.github.io/pictures/FoMo2025.jpg">

Course <a href="http://uvafomo.github.io/">website</a>.
