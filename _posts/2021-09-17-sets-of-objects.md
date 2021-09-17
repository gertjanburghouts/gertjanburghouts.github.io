---
layout: post
title: "Scenes as Sets of Objects"
date: 2021-09-17 11:00:00 -0000
categories: deep sets
excerpt_separator: <!--more-->
---

In one of our projects, a robot is searching rooms for persons, in a search and rescue setting. 
The person may have fallen behind a couch, and therefore invisible. 
Can we infer whether it is likely that a person is in the current room, based on the observed objects? 
Quite well, see the illustrations below!

One challenge is that the number of objects varies from scene to scene. 
That is why we need to model sets, read more by clicking on this post.

<img src="https://gertjanburghouts.github.io/pictures/sets_of_objects_predictions.jpg" width="80%">
     
<!--more-->

We have deployed a deep learning model on sets: Deep Sets. 
It takes the set of object labels and their relative position and size as inputs. 
It produces the likelihood that a person may be present. 

<img src="https://gertjanburghouts.github.io/pictures/sets_of_objects_model.jpg" width="80%">

In the illustrated results, no person was present. 
How to learn this? 
We did a trick: we used images in which there were people present, but masked them out from the training set, by excluding the person labels from each set of objects. 
