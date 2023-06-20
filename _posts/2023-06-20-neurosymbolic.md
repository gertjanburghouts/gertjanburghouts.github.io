---
layout: post
title: "Neuro-Symbolic Programming"
date: 2023-06-20 17:00:00 -0000
categories: neuro-symbolic AI
excerpt_separator: <!--more-->
---

How to find door handles inside a house, while many other things in the house look like handles? Not straightforward! Especially if your model is uncertain about its predictions about doors and handles.

Neuro-symbolic programming to the rescue. It can leverage expert knowledge on top of deep learning models. It enables probablistic reasoning, taking into account uncertainties. You have to define the situation of interest by first-order logic. This is nice because it is symbolic. The good part is that you don't have to keep track of all hypotheses and variables yourself, the program will do this for you. As inputs it takes all of the predictions, even the ones with low confidence. The program will do the sense-making for you.

<img src="https://gertjanburghouts.github.io/pictures/neurosymbolic-usecases.jpg">

You do not even need to train the underlying deep learning model(s), because you can use vision-language models in a zero-shot manner. That is, the neuro-symbolic program is agnostic about where the input predictions come from. Therefore I also see a strong potential when there are different models that need to be interpreted. These models can even come from different data modalities or platforms.

The illustration shows various examples from finding two abandoned helicopters in satellite images and helping SPOT to find the handle that opens the door.

Such a neuro-symbolic program can also be improved after user feedback. This optimization can be done with as few as 7 feedbacks only about yes/not interesting. Gaussian Process optimization is effective to boost the program's performance.
