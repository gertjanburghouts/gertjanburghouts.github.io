---
layout: post
title: "Neural Networks are Graphs"
date: 2023-09-18 07:00:00 -0000
categories: neural network graph
excerpt_separator: <!--more-->
---

Neural networks are actually graphs, i.e. computation graphs. 

At the TAG workshop at ICML, we showed that interesting properties about a neural network can be learned from the network's weights. 
For instance, representing each image as a single neural network (SIREN), and then learning a label from those networks' weights, to classify the image. 

<img src="https://gertjanburghouts.github.io/pictures/nns_are_graphs.jpg">

Although this is a detour, it is interesting research, because it paves the way for more advanced analyses of neural networks. 
For instance, recently other researchers have predicted the robustness of neural networks based on their weights. 
