---
layout: post
title: "Multiset Prediction"
date: 2022-04-22 15:00:00 -0000
categories: set prediction equivariance
excerpt_separator: <!--more-->
---

Sets are everywhere: the objects in an image {car, person, traffic light}, the atoms in a molecule, etc.
We research set prediction: how can a neural network output a set?
This is not trivial, because sets can differ in size.
The neural network needs to deal with variable-sized outputs.
See our ICLR 2021 paper for an energy-based approach.

<img src="https://gertjanburghouts.github.io/pictures/iclr22_poster_neural_network.jpg" width="50%">

In our ICLR 2022 paper, we extend the method to deal with multisets.
Contrary to sets, multisets can have multiple occurrences of a single element.
For instance, {car, car, person, person, person, traffic light}.
In multisets, elements may be identical, which poses a problem if we would like to get a different output for them.
For instance, if we have {car, car} and we want to output the label and ordering {car-1, car-2}.
Previous approaches are based on sets and cannot treat car-1 and car-2 differently.

We propose a method that can treat car-1 and car-2 differently, to output {car-1, car-2}. 
This essential ingredient is called multiset-equivariance. 
Published at ICLR 2022 and presented on May 25 2022.

This proves to be very helpful, not only to separate equal elements, but also similar elements.
This property boosts the performance for both set and multiset prediction. 
Performance is favorable over Transformer and Slot Attention.
In the example below, you see the prediction of objects and their properties, and how our method (last column) improves by refining iteratively (from left to right). 

<img src="https://gertjanburghouts.github.io/pictures/iclr22_poster_clevr.jpg" width="50%">

Part of NWO Efficient Deep Learning, co-sponsored by TNO Appl.AI.

<!--more-->


