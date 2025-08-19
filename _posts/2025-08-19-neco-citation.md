---
layout: post
title: "DINO v3 builds on our work!"
date: 2025-08-19 06:00:00 -0000
categories: self-supervised learning transformer patches foundation models
excerpt_separator: <!--more-->
---

DINO v3 has been released. And it builds on our recent ICLR 2025 paper! 

Our method, NeCo, improved the DINO patch-level features by self-supervised post-training. 
We enforced that the patches in two views of the same image (i.e. different augmentations) follow the same ordering, relative to an external memory set of representative image patches. 
This ordering proves to be a very strong learning signal: it is much stronger than just looking at the nearest neighbors only, or looking at clusters of patches in embedding space. 

<img src="https://gertjanburghouts.github.io/pictures/neco_segmentation.jpg">

Proud that it was cited by DINO v3!
