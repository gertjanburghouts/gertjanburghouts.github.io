---
layout: post
title: "Explainability of Predictions"
date: 2022-06-19 18:00:00 -0000
categories: explainable AI set prediction
excerpt_separator: <!--more-->
---

I'm curious about deep learning and why it makes particular decisions. 

Q1. How little of a picture does such a model need for a particular classification? 
A1: For an ambulance, you only need to see a piece of will and a red stripe (see attached video).

Q2. Which parts of a picture lead the model to a different classification? 
A2.1: An ambulance becomes more like a fire truck, if the red cross, the letters 'ambulance' and a few letters of 'ambulance' are not visible. 
A2.2: If the red stripes, the door, and the blue health symbol are not there, then an ambulance becomes the police car.

Check out the demo:

<iframe width="500" height="184" src="https://www.youtube.com/embed/KQ271xKabv0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

You see three types of vehicles: an ambulance, fire truck, or police car. 
For each picture, a part of the picture is first removed, as long as the classification remains the same (Q1). 
Later on, patches are removed to arrive at a different classification (Q2).

Key observations: (1) All these pictures were convertible to *any* other class! 
(2) Logos are important. 
(3) Specific details are important too, such as grill in the front, red lamp, or blue color. 
(4) Regularly, the predictions are based on very limited visual evidence. 

For this experiment, an image was modeled as a bag of patches, encoded by a set prediction model. 
Modeling it as a set, enables us to remove patches (i.e., set elements) and still do predictions. 
The model can deal with a variable amounts of inputs.
