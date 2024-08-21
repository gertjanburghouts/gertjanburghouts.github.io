---
layout: post
title: "Guiding Segment-Anything Model (SAM)"
date: 2024-08-21 06:00:00 -0000
categories: semantic segmentation transformer patches
excerpt_separator: <!--more-->
---

Localizing object parts precisely is essential for tasks such as object recognition and robotic manipulation. 
Recent part segmentation methods require extensive training data and labor-intensive annotations. 
Segment-Anything Model (SAM) has demonstrated good performance on a wide range of segmentation problems, 
but it requires (manual) positional prompts to guide it where to segment. 
Furthermore, since it has been trained on full objects instead of object parts, 
it is prone to over-segmentation of parts. 

To address this, we propose a novel approach that guides SAM towards the relevant object parts. 
Our method learns positional prompts from coarse patch annotations that are easier and cheaper to acquire. 
We train classifiers on image patches to identify part classes and aggregate patches into regions of interest (ROIs) with positional prompts. 
SAM is conditioned on these ROIs and prompts. 

We call our method 'Guided SAM'. 
It enhances efficiency and reduces manual effort, allowing effective part segmentation with minimal labeled data. 
It improves the average IoU on state of the art models from 0.37 to 0.49, while requiring five times less annotations.

<img src="https://gertjanburghouts.github.io/pictures/guidedSAM.jpg">

Part of the FaRADAI project. 
Accepted at International Conference on Pattern Recognition, 2024.
