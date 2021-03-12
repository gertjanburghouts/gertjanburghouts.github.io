---
layout: post
title: "Weighting evidence by thrustworthiness"
date: 2021-03-12 11:00:00 -0000
categories: object parts robustness
excerpt_separator: <!--more-->
---

Our aim is to increase the autonomy of the SPOT robot. Our research covers perception, planning and self management. 
For perception, one of the challenges is to understand objects, even when they are novel or not seen before. 
Novel objects are detected by recognizing and combining their parts. 

But not all parts are equally discriminative or robust. 
This post is about combining evidence in a more principled way, by taking the evidence for each part into account. 

The coloring of the nodes in the part-hierarchy shows that some parts are more thrustworthy (e.g., head) than others (e.g., lower arm).

<img src="https://gertjanburghouts.github.io/pictures/weighting_evidence.jpg">

<!--more-->

A high confidence somewhere in the taxonomy, propagated too much to the overall confidence. 
Even if that part of the taxonomy was considered not that trustworthy. 
A proper weighting of evidence was needed. 
Ideally, by taking into account the trustworthiness of each bit of evidence. 
This indeed leads to better predictions than the previous model, which was sometimes over-confident.
The histograms of its confidences show that the new model better predicts when the object is indeed present (higher confidence) or not (low confidence).

<img src="https://gertjanburghouts.github.io/pictures/better_separation.jpg">

Example predictions are shown below,

<img src="https://gertjanburghouts.github.io/pictures/example_results.jpg">

This research is supported by the project Appl.AI SNOW 2021.
