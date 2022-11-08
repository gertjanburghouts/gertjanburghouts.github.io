---
layout: post
title: "Searching for Images using Semantics"
date: 2022-11-08 09:00:00 -0000
categories: semantics language vision clustering
excerpt_separator: <!--more-->
---

Suppose you are given a huge set of images. But you do not know what is in them.
How do you start?

<img src="https://gertjanburghouts.github.io/pictures/semantic-clip-search.jpg">

We have developed a method to cluster images and give each cluster a meaningful name. 
For each image, we assign an initial label from a large set of candidate words.
We do this by a language-vision model: CLIP from OpenAI.

<img src="https://gertjanburghouts.github.io/pictures/cluster-naming.jpg">

Next, we look for the word that best describes all images in the cluster.
Possibly that could be a container name.
We look into the coarse-to-fine hierarchy of all labels in the cluster, taken from Wordnet.
In this way, we can assign Bird to a cluster containing images of Swans, Owls and Parrots.
