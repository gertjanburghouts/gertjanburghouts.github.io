---
layout: post
title: "100 Citations for ProtoProp: Recognising What You've Never Seen"
date: 2026-11-20 05:00:00 -0000
categories: zero-shot graph neural network neurips
excerpt_separator: <!--more-->
---

Our NeurIPS 2021 paper on ProtoProp has just passed 100 citations. 
Many thousands of AI papers come out every year, so we are very proud. 

Independent Prototype Propagation for Zero-Shot Compositionality. F. Ruis, G.J. Burghouts, D. Bucur. NeurIPS, 2021.

The question behind the paper is easy to ask and hard to answer: how do you recognise something you have never seen? 
A model that has seen yellow spheres and red cubes should still recognise a yellow cube. 
That is zero-shot compositionality: recognising new combinations of known shapes and attributes.

The figure shows the idea. 
ProtoProp learns from the combinations it has seen (left). 
It untangles them into separate prototypes for colour and for shape (middle). 
Then it recombines those prototypes to recognise combinations it has never seen (right).

<img src="https://gertjanburghouts.github.io/pictures/protoprop-100.png">

ProtoProp works in three steps:
- Learn a prototype for every attribute (yellow, wet, sliced) and every object (cube, shoe, apple).
- Keep those prototypes independent. In training data, attributes and objects are correlated. If "yellow" mostly appears on spheres, a naive "yellow" prototype secretly encodes "sphere". An independence constraint makes each prototype capture only its own concept.
- Propagate them through a compositional graph. A graph neural network turns the attribute and object prototypes into prototypes for all combinations, including unseen ones. To recognise an object, the model finds the nearest combination prototype.

The independence step made the difference. It stops the model from carrying spurious correlations from seen pairs into unseen ones.

The paper grew out of our work for DARPA's Learning with Less Labels program.
