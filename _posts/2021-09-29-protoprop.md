---
layout: post
title: "Our paper is accepted at NeurIPS!"
date: 2021-09-29 08:00:00 -0000
categories: compositional graph zero-shot learning
excerpt_separator: <!--more-->
---

We want Deep Learning models that generalize beyond previous observations. 
Someone who has never seen a zebra before, could nevertheless recognize one when we tell them it looks like a horse with black and white stripes. 
Standard Deep Learning cannot do that. 

In DARPA's Learning with Less Labels, together with University of Twente, we have developed the ProtoProp model. 
Our model is compositional: it recombines earlier knowledge. 

<img src="https://gertjanburghouts.github.io/pictures/ProtoProp.jpg">

The <a href="https://arxiv.org/abs/2106.00305">paper</a> is accepted at NeurIPS.

(read more by clicking the post)

<!--more-->

We learn prototypical representations of visual primitives in the form of objects (e.g., horse) and attributes (e.g., stripes). 
We optimize these prototypes to be conditionally independent, to 'unlearn' the spurious correlations. 
For instance, a horse is typically on grass (a correlation between object and context), but green is not an actual property of horse (no causal relation).  

A compositional graph combines the prototypes and learns to propagate them to novel, unseen classes (zebra = horse + stripes). 
We outperform previous methods on two common CZSL benchmarks, on both seen and unseen classes, but especially on the unseen classes.

The full paper is on <a href="https://arxiv.org/abs/2106.00305">Arxiv</a>. 
Empowered by DARPA LwLL. 
Joint research with Doina Bucur of the University of Twente.
