---
layout: post
title: "Incrementally Learning the Affordances of New Objects"
date: 2024-10-27 10:00:00 -0000
categories: affordance inference incremental learning markov logic network
excerpt_separator: <!--more-->
---

A banjo can be grasped, because most musical instruments can be grasped, and it has a low weight so it can be moved and lifted. 
We have devised a method that can incrementally learn such affordances, also for new objects. 
It leverages the knowledge it has so far (e.g. most musical instruments can be grasped) and combines it with new evidence for new objects (e.g. a banjo has a low weight). 
The challenge: how to update knowledge & when to change beliefs. 

We developed a Markov Logic Network (MLN) variant, called MLN-CLA (cumulative learning algorithm) that can do this. 
Some things are often true, but not always. 
The belief of MLN-CLA is stronger when there is more evidence towards a hypothesis. 
This is expressed in weights of the formulas that the MLN learns. 

After having seen some objects over time, it learns the right affordances for most objects. 
The figure shows how this learning improves over time. 

<img src="https://gertjanburghouts.github.io/pictures/irc_2024_mln_incr.png">
