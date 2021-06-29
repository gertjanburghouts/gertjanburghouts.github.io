---
layout: post
title: "Compositionality of objects and attributes"
date: 2021-06-29 11:00:00 -0000
categories: zero-shot learning
excerpt_separator: <!--more-->
---

Humans are good at compositional zero-shot reasoning; 
Someone who has never seen a zebra before could nevertheless recognize one when we tell them it looks like a horse with black and white stripes. 

Machine learning systems have difficulty with compositionality. 
We propose a method that uses a graph that captures knowledge about compositions of objects and their attributes, 
and learn to propagate through the graph, such that unseen classes can be 
recognized based on their composition of known attributes. 

<img src="https://gertjanburghouts.github.io/pictures/protoprop.jpg">

<!--more-->

In this work, three of our Deep Learning focus areas come together: 
learning with less labels (zero-shot), learning with knowledge (knowledge graph) and learning with structure (graph propagation). 
Work carried out by student Frank Ruis in the DARPA Learning with Less Labels (LwLL) project in collaboration with University of Twente (Doina Bucur). 

Paper is on  <a href="https://arxiv.org/abs/2106.00305">Arxiv</a>.
