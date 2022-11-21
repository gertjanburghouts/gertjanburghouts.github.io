---
layout: post
title: "Creating a Deep Learning Model without Labels using Semantics"
date: 2022-11-21 08:00:00 -0000
categories: zero-shot semantic transfer
excerpt_separator: <!--more-->
---

Sometimes we do not have any images, let alone labeled images, for the particular class that we are interested in.
But there are tons of labeled data about classes that are related.
We re-use classifiers on those related classes to infer the class of interest.

For instance, localizing a Kart.
Our method finds that Car, Motorbike and Skateboard are very related to Kart.
We establish this by Optimal Transport.
We reconstruct an object model (Faster R-CNN) for Kart by recombining the weights of Car, Motorbike and Skateboard.

<img src="https://gertjanburghouts.github.io/pictures/zero-shot-object-detection-v2.jpg">

This makes it possible to localize related objects without having to label or learn anything.
Work sponsored by DARPA Learning with Less Labels. 
