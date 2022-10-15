---
layout: post
title: "Learning a Model from Stable Diffusion"
date: 2022-11-30 09:00:00 -0000
categories: image generation synthetic trainset
excerpt_separator: <!--more-->
---

There is a revolution going on in the field of image generation.
Stable diffusion, Dall-E and Imagen make it possible to create images from a textual description.
We were wondering whether such images may serve as a training set.

<img src="https://gertjanburghouts.github.io/pictures/stable_diffusion.jpg">

Well, it may work, but only for simple cases such as the blue and red jeeps and cars below.
The problem with more advanced cases is that the images may be weird or implausable.
Of course, you could have a human in the loop, to remove such problematic images. 
