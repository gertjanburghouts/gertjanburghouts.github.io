---
layout: post
title: "Cycle Consistency for Multi-Camera Matching"
date: 2024-12-12 08:00:00 -0000
categories: cameras multiple views matching self-supervision
excerpt_separator: <!--more-->
---

Matching objects across partially overlapping camera views is crucial in multi-camera systems and requires a view-invariant feature extraction network. But labelling in several cameras is labor-intensive. We rely on self-supervision, by making cycles of matches, from one camera to the next and back again. The cycles can be constructed in many ways. We diversify the training signal by varying the cycles. 

<img src="https://gertjanburghouts.github.io/pictures/cycle_consistency.jpg">

We achieve a 4.3 percentage point higher F1 score. Especially when there is limited overlap in camera views, the matching is improved. 

<img src="https://gertjanburghouts.github.io/pictures/cycle_consistency_result.jpg">

Accepted at International Conference on Computer Vision Theory and Applications (VISAPP) 2025. See publications.
