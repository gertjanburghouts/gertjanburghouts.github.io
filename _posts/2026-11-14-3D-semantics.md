---
layout: post
title: "In 3D, Don’t Average Away the Details"
date: 2026-11-14 05:00:00 -0000
categories: 
excerpt_separator: <!--more-->
---

From one side, a black mug is just a dark cylinder. Turn it, and a red Chinese character appears. For someone with a visual impairment exploring a room through an assistive system, that detail matters. Most 3D scene understanding methods lose it, because they merge features from many frames into one representation.

We keep the views instead. Our training-free framework takes a handheld video and a query like “black mug.” It works in four steps:

- Find every matching object with SAM 3.
- Select a small set of sharp, diverse views, dropping blurry and redundant frames.
- Reason across those views with a vision-language model. It writes a detailed description and picks the most informative view.
- Show where the object is in a 3D reconstruction of the room.

You get a description, a picture to back it up, and a location.

In a case study of a cluttered living room, our approach produced more accurate and more detailed descriptions than a LangSplatV2-based baseline: 0.67 vs 0.50 precision and 0.68 vs 0.56 recall. It found the mug’s red character, while the baseline reported “no readable text or logos visible.” It also kept working with very few frames.

<img src="https://gertjanburghouts.github.io/pictures/3D-semantics.png">
