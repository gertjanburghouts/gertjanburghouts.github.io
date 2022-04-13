---
layout: post
title: "Domain-specific Pretraining"
date: 2021-04-13 10:00:00 -0000
categories: pretraining dataset domain transfer object detection
excerpt_separator: <!--more-->
---

We often retrain a deep learning model for a new domain and new classes. 
For instance, object detection in images that were recorded from above (overhead). 
These overhead images look very different from common datasets with (mostly) frontal images. 
Sometimes the classes are also different, such as swimming pools that become visible in overhead images. 

<img src="https://gertjanburghouts.github.io/pictures/dota_1.5_1.jpg">

For that purpose, we need to retrain the model. Preferably with as few labels as possible. 
Selecting a proximal dataset (labeled overhead images) is very helpful. 
We used DOTA 1.5, a big overhead dataset, as pretraining. 
We were able to improve the Pool-Car dataset accuracy from mAP=0.14 to mAP=0.33 with just 1 label per class.

<img src="https://gertjanburghouts.github.io/pictures/dota_1.5_2.jpg">

Part of our research in DARPA Learning with Less Labels.
