---
layout: post
title: "Aerial Image Segmentation"
date: 2023-09-12 07:00:00 -0000
categories: aerial images image segmentation
excerpt_separator: <!--more-->
---

Image segmentation is key to distinguish the various elements that are in a visual scene. 
Common models are trained on frontal views, which does not work for aerial images. 
To train a model for aerial images, a lot of labeled images are required, and labeling of segmentations is time-consuming. 

We propose to make clusters of image segments and to label only those clusters. 
The clustering is based on spatial feature maps, taken from intermediate embeddings of a self-supervised model. 
Labeling clusters is very easy and takes almost no time. 

<img src="https://gertjanburghouts.github.io/pictures/aerial-segmentation.jpg">

Here you see a result of 50 such labels. 
Not perfect, but already useful, while only requiring a few minutes.  
