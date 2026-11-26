---
layout: post
title: "FIND: Making Foundation Models Work in the Field"
date: 2026-11-26 05:00:00 -0000
categories: foundation-models robotics remote-sensing find
excerpt_separator: <!--more-->
---

FIND (Foundation for Industry) is an NWO Perspectief programme on large AI models for a resilient high-tech industry. 
TNO takes part for robotics and autonomy, and we co-supervise two of its PhD researchers. 
We made a poster about our work in FIND.

Foundation models are trained on everyday web images. 
Robots, drones and satellites see a different world, and must act on what they see. 
FIND targets that gap: data and applications that current foundation models serve poorly, with models that can run on edge devices.

<img src="https://gertjanburghouts.github.io/pictures/FIND_poster.jpg">

Five questions drive our work:
- Is this sample out of domain? A model should signal when it cannot predict properly. Attention sinks let open-vocabulary detectors admit that an object is not there (ICLR 2026).
- Does it know what to do here? We predict a traversability map around the robot, so it knows where it can go, and when to look closer or ask.
- Is something dangerous? Danger sits in the relations between objects. We put first-order logic on top of foundation models, so a user can ask in plain language.
- Can it run on the robot? We want one model that scales to the compute budget at hand. Pruning half of DINOv3 costs only 0.8% ImageNet accuracy, without retraining.
- What about satellite images? Our neurosymbolic model RUNE beats large vision-language models at retrieving satellite images for complex queries (ACM TSAS 2026).

Across these questions, we adapt foundation models in four ways, from outside the model to inside it: pre- and post-processing, steering, re-learning a part, and changing the model itself.
