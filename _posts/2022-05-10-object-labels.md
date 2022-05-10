---
layout: post
title: "How to select first labels for object detection?"
date: 2022-05-10 09:00:00 -0000
categories: active learning object detection
excerpt_separator: <!--more-->
---

Learning object detection models with very few labels, is possible due to ingenious few-shot techniques, and due to clever selection of images to be labeled.
Few-shot techniques work with as few as 1 to 10 randomized labels per object class.

We are curious if performance of randomized label selection can be improved by selecting 1 to 10 labels per object class in a non-random manner.
Our method selects images to be labeled first.
It improves 25% compared to random image selection!

Below you see the first images, selected by our method, to be labeled.
These are representative and the object is well visible yet not too large.

<img src="https://gertjanburghouts.github.io/pictures/label_selection.jpg" width="80%">

The paper is accepted for International Conference on Image Analysis Processing and presented next week. 
This research is part of DARPA Learning with Less Labels. 
More information when clicking on the post. 

<!--more-->

Several active learning techniques have been proposed to select object labels, but all started with a minimum of several tens of labels.
We explore an effective and simple label selection strategy, for the case of only 1 to 10 labels per object class.

First, the full unlabeled dataset, without any labels, is clustered into N clusters, where N is the desired number of labels.
Clustering is based on k-means on embedding vectors from a state-of-the-art pretrained image classification model (SimCLR v2).
The image closest to the center is selected to be labeled.

It is effective: on Pascal VOC we validate that it improves over randomized selection over 25%, with large improvements especially when having just 1 label per object class.
We have several benefits to report on this simple strategy: it is easy to implement, it is effective, and it is relevant in practice where one often starts with a dataset without any labels.
