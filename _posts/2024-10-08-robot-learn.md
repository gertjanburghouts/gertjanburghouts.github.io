---
layout: post
title: "Robot Learns on the Job"
date: 2024-10-08 04:00:00 -0000
categories: robot learning
excerpt_separator: <!--more-->
---

Robots in the open world will encounter new situations, 
which may lead to lower performance. 
For instance, it may not recognize the desired object, 
such as a different type of door handle. 
We devised a framework in which the robot can learn on the job. 

The user is the robot operator, he/she can indicate the object by clicking on it. 
With the current model, we do a best-effort in estimating the box for that location. 
This box is used for retraining the model. 
Of course, we do not want to forget the previous objects. 
To that end, we modified Grounding DINO's tokenizer, to only update the relevant tokens, from our ICPR 2024 paper. 
We applied this on SPOT, where the model can now successfully learn new objects.  

<img src="https://gertjanburghouts.github.io/pictures/robot_learn_azure.jpg">
