---
layout: post
title: "How to Open the Door?"
date: 2023-09-25 07:00:00 -0000
categories: affordances reasoning
excerpt_separator: <!--more-->
---

It seems like a simple question: how to open the door? 
But for a robot such as SPOT, this is not easy. 
Doors can be opened by various openers, from handles to knobs and push bars. 
It matters a lot for the robot, because it needs to perform a different action for each opener - i.e. how to grasp and move it. 

<img src="https://gertjanburghouts.github.io/pictures/handle_clustering.jpg">

With a language-vision model, we were able to detect the various openers. 
But it was not able to distinguish between them, because language is not precise enough. 

With a clustering technique, we were quickly able to make the distinction. 
In the image, you can see that the different door openers are clustered together. 
The different clusters are indicated by their center, which is most representative. 
This is visualized by the images with the box around them. 
