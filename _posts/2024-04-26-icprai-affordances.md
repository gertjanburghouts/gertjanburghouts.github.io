---
layout: post
title: "Efficient Correction of Vision-Language Models"
date: 2024-04-26 09:00:00 -0000
categories: affordance detection vision language model
excerpt_separator: <!--more-->
---

For robotics, vision-language models (VLMs) are the go-to, because they have zero-shot capabilities. 
They can look for new objects based on textual prompts, which often works surprisingly good. 
But, not always... 

We investigated whether a VLM, GLIP, can be used to find doors and their openers. 
It can do a pretty good job, but it's far from perfect. 

<img src="https://gertjanburghouts.github.io/pictures/icprai_affordances.jpg">

So, we let the robot do its best, to find as most as it can. 
Next, we involve the user to correct the wrong predictions. 
Finally, the model is retrained with the corrections. 

This is a very effective strategy. 
The user only needs to label a few instances, i.e. the mistakes. 
This is very efficient. 

The paper was accepted at International Conference on Pattern Recognition and Artificial Intelligence (ICPRAI).
