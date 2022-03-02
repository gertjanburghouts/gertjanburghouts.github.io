---
layout: post
title: "Set Prediction by an Energy-based Model"
date: 2022-03-02 15:00:00 -0000
categories: set prediction energy-based model
excerpt_separator: <!--more-->
---

Which celebrities have something in common?
Please have a look at the top row in this image.

<img src="https://gertjanburghouts.github.io/pictures/set_prediction.jpg" width="80%">

Which attributes do they share?
It depends on how you look!

We developed a new deep learning model that is able to predict multiple answers.
This is key to questions that are inherently ambiguous.

Each row in the attached image is one answer.
In total, the model produces four answers.
Blue indicates the celebrities who are not sharing two attributes.
These four answers by the model are correct.
Row 1: man and no beard.
Row 2: man and glasses.
Row 3: man and bold.
Row 4: bold and glasses.

Paper at ICLR '21 with David Zhang and Cees Snoek (University of Amsterdam). 
More information when clicking on the post.

<!--more-->

The attributes that were considered in this experiment are: bald, bangs, blond hair, double chin, eyeglasses, goatee, gray hair, male, no beard, wearing hat, wearing necktie.
The model has never been told anything about attributes.
The only thing that the model is told: who share some attributes and who don’t.

The science is about whether a model is able to (a) learn implicit commonalities between subsets, and, (b) predict multiple plausible answers.
It is based on a deep energy-based model, which learns an energy landscape with possibly multiple minima, representing the various plausible predictions.
The F1 score on the celebrities experiment is 0.73.
This is very promising given the complexity of the task.

This research is part of the NWO Efficient Deep Learning program, and co-funded by Appl.AI.
