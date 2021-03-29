---
layout: post
title: "Patent granted: Sequence Finder"
date: 2021-03-29 09:00:00 -0000
categories: long-term activity recognition
excerpt_separator: <!--more-->
---

The innovation is called Sequence Finder. 
This algorithm finds temporal patterns (e.g., making a coffee) by propagating confidences (not binary!) 
about shorter-term activities (e.g., taking cup, pooring milk, turning on coffee machine).

<img src="https://gertjanburghouts.github.io/pictures/sequence_finder.jpg">

<!--more-->

This research was part of the ADREM project. The goal was to start with a human specification 
of a long-term human activity as a composition of short-term activities. The algorithm learns the 
short-term activities and combines that into a single confidence of the long-term activity.

The illustration below shows an example of somebody who was refused entry to a building: 
a sequence of approach, loiter, leave. Continuous confidences for each activity are traced 
through time and combined into a single confidence about the complete pattern.
