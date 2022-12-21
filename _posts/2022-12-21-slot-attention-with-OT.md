---
layout: post
title: "Slot Attention with Optimal Transport"
date: 2022-12-21 09:00:00 -0000
categories: slot attention optimal transport object discovery
excerpt_separator: <!--more-->
---

To discover objects without having an explicit model for them, Slot Attention is a very powerful technique. 
Yet, it may have trouble with separating objects (into different 'slots'), when they are highly similar.

To improve separability, we build in a step to improve the discrimination of the learned features, by optimal transport. 
It helps to notice subtle differences.

<img src="https://gertjanburghouts.github.io/pictures/slot-attention-with-OT.jpg">

Paper at NeurIPS workshop on Neuro Causal and Symbolic AI (nCSI), 2022 (Oral).
