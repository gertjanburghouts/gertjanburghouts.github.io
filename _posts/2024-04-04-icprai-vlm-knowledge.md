---
layout: post
title: "Affordance Perception"
date: 2023-12-08 09:00:00 -0000
categories: image classification zero shot prior knowledge
excerpt_separator: <!--more-->
---

Mobile robot platforms will increasingly be tasked with activities that involve grasping and manipulating objects 
in open world environments. Affordance understanding provides a robot with means to realise its goals and 
execute its tasks, e.g. to achieve autonomous navigation in unknown buildings where it has to find doors 
and ways to open these. In order to get actionable suggestions, robots need to be able to distinguish subtle 
differences between objects, as they may result in different action sequences: doorknobs require grasp and twist, 
while handlebars require grasp and push.

We improve affordance perception for a robot in an open-world setting. Our contribution is threefold: 
(1) We provide an affordance representation with precise, actionable affordances; 
(2) We connect this knowledge base to a foundational vision-language models (VLM) and 
prompt the VLM for a wider variety of new and unseen objects; 
(3) We apply a human-in-the-loop for corrections on the output of the VLM. 

<img src="https://gertjanburghouts.github.io/pictures/icprai_vlm_knowledge_2024.png">

The mix of affordance representation, image detection and a human-in-the-loop is effective 
for a robot to search for objects to achieve its goals. We have demonstrated this in a scenario of 
finding various doors and the many different ways to open them.

The paper was accepted at International Conference on Pattern Recognition and Artificial Intelligence (ICPRAI).
