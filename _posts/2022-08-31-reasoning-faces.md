---
layout: post
title: "Neuro-Symbolic Reasoning"
date: 2022-08-22 16:00:00 -0000
categories: reasoning first-order logic symbolic predicates
excerpt_separator: <!--more-->
---

Deep learning becomes more and more capable of detecting objects, classifying them, describing their attributes. 
This enables reasoning about such objects, their specifics, and relations! 

For instance, see the photo of my research group at TNO. 
Can you find a woman standing next to a man, both wearing glasses? 

<img src="https://gertjanburghouts.github.io/pictures/reasoning-faces.jpg">

First-order logic is able to describe this in a few lines of symbolic predicates. 
We recognize the symbols in the predicates via a language-vision model (CLIP). 
A neuro-symbolic program reasons about the logic and the recognized symbols with their probabilities. 

This reasoning is probabilistic and multi-hypothesis with pruning. 
A crucial asset, if you have many objects that may sometimes be uncertain. 

The result is highlighted. 
Pretty cool, right?
