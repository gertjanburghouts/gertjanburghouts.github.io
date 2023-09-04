---
layout: post
title: "Transferring Knowledge to New Classes"
date: 2023-09-04 07:00:00 -0000
categories: zero shot semantic transfer
excerpt_separator: <!--more-->
---

Sometimes for a new class there are no training samples yet. 
This makes the standard supervised learning procedure impossible.
To correctly classify a new class, prior knowledge about that class is required.

<img src="https://gertjanburghouts.github.io/pictures/cub_reconstruction.jpg">

We leverage ChatGPT's descriptions of classes.
Via language models we reconstruct the new class via sparse linear estimation.

Very effective: on CUB with 200 bird classes, it achieves an accuracy of 62%.  
It also provides a kickstart for further learning when few images of the class become available.  
