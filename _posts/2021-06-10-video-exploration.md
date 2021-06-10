---
layout: post
title: "Interactive Video Exploration
date: 2021-06-10 13:00:00 -0000
categories: video graphical interface t-SNE embeddings
excerpt_separator: <!--more-->
---

Video exploration of persons and activities

Looking for particular concepts in a large set of videos or images is very relevant with today's amounts of data. 
A correct way of visualizing by plotting similar instances close together, really depends on what you're looking for. 
When searching for a particular person, the similarity should be based on people's appearances, whereas for activities it should be based on motion patterns.

<img src="https://gertjanburghouts.github.io/pictures/tsne-viewer.jpg">

<!--more-->

In our viewer, it is possible to switch. 
In the example below, the starting point is a person of interest. 
This person has appeared several times in different videos. These moments are grouped together in the 2D visualization (t-SNE on embeddings). 
By clicking on these moments, one is able to see his activities. 
This is helpful for making reconstructions of an event over longer time and possibly multiple locations.
