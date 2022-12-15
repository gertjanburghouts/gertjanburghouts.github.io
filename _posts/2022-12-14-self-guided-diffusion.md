---
layout: post
title: "Self-Guided Diffusion"
date: 2022-12-14 09:00:00 -0000
categories: image generation diffusion self supervision
excerpt_separator: <!--more-->
---
 
There is a revolution going on in the field of image generation.
It was shown that such images get better when guiding them, e.g., with a textual description or semantic token from another classifier.
We were curious whether we can guide them also with a self-supervised learning signal.

<img src="https://gertjanburghouts.github.io/pictures/self-guided-diffusion.jpg">

We use self-learned bounding boxes from another method to serve as guidance for the generation.
That works nicely!
It creates images with similar semantic content, see the illustration for some example results.  

Paper at NeurIPS workshop on Self-Supervised Learning: Theory and Applications, 2022.
