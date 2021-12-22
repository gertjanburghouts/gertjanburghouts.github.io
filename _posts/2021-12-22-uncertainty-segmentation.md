---
layout: post
title: "Uncertainty of Predictions"
date: 2021-12-22 11:00:00 -0000
categories: hyperspherical equidistant prototypes
excerpt_separator: <!--more-->
---

Knowing the uncertainty of a prediction by a deep learning model is key, if you want to base decisions on it. 
Especially in an open world, where not everything can be controlled or known beforehand. 

We have modeled prototypes that are maximally apart, so the unknown samples have maximum likelihood of falling in the in-between spaces. 
Indeed, out-of-distribution samples have a larger distance to the prototypes. 
The distance is a good proxy of uncertainty. 

This work was published in NeurIPS workshop on Deployable Decision Making (DDM).
The illustration shows image segmentation and the uncertainty of the predictions per pixel. 

<img src="https://gertjanburghouts.github.io/pictures/segmentation_uncertainty.png" width="80%">

This research is part of TNO's Appl.AI program. It is a collaboration of Intelligent Imaging and Automotive department (Helmond).
