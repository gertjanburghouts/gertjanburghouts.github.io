---
layout: post
title: "Neuro-Symbolic Programming for Anomaly Detection"
date: 2022-10-30 09:00:00 -0000
categories: outlier anomaly relevancy
excerpt_separator: <!--more-->
---

Our aim is to find an anomaly in an image, based on prior knowledge about the involved objects and their relations. 
A disadvantage of data-driven anomaly detection (statistical outlier models), is that they may produce anomalies that are not relevant at all.  
In contrast, we specify anomalies in order to make sure that they are relevant. 
An overview of our method is shown below. 

<img src="https://gertjanburghouts.github.io/pictures/zero-shot-neuro-symbolic.jpg">

At the top, it shows how an anomaly such as 'tool on floor' is translated into 
symbolic predicates such as object(o, tool), segment(x, floor) and above(o, x). 
At the bottom left, the figure shows how the symbols from the predicates, 
such as 'tool' and 'floor', are measured from images by zero-shot language-vision models. 
These measurements are transformed into probabilistic facts, 
which are fed to the neuro-symbolic program in order to be validated against the logic (bottom right). 

Our paper is accepted at IROS Probabilistic Robotics 2022 (Kyoto).
