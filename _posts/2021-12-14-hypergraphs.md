---
layout: post
title: "Hypergraph Prediction"
date: 2021-12-14 11:00:00 -0000
categories: recurrent graph neural network
excerpt_separator: <!--more-->
---

Predicting graphs is becoming popular, as many problems are structural and can be expressed as a graph.
For instance, relations between objects in a scene.
Often, the relations are multi-way, beyond standard graphs with edges that connect two nodes.
Connecting multiple nodes requires hypergraph prediction.
We propose to do this in a recurrent way, at each step refining the predicted hypergraph.

<img src="https://gertjanburghouts.github.io/pictures/hypergraphs.jpg" width="80%">

<!--more-->

Our recent research does this by an iterative refinement through a recurrent neural network.
For computationally complex problems, such as finding a convex hull of points in a high-dimensional space, the deterministic solutions are often also iterative (e.g., quick hull).
We are inspired by iterative refinement for our neural network solution.

Another issue is that for n inputs, there can be 2^n hyperedges (i.e., possible subsets of connected nodes).
This is the reason why existing methods are not scalable to large n.
We propose to use a truncated incidence matrix.
The incidence matrix is a convenient representation, as typically the number of hyperedges will be much lower (no need to represent all possibilities), so the matrix is sparse and it can be truncated to the expected amount of hyperedges.

This research is part of the NWO Efficient Deep Learning program, and co-funded by Appl.AI.
