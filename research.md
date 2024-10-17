---
layout: page
title: Research
permalink: /research/
---

My research focuses on deep learning for situation understanding, embed AI models on robots, and to include logic and prior knowledge in the learning process.

<img style="padding: 2%; float: right;" src="https://gertjanburghouts.github.io/pictures/presenting.jpg" width="20%">

**Adapting Foundation Models**

Foundation models are a great promise. Due to their broad pretraining they have acquired a lot of knowledge about the visual and semantic world. Yet they often lack specialized concepts. We extend foundation models with new concepts, without forgetting (e.g. incremental learning with Grounding DINO). Moreover, we steer them to focus on the right parts of the image (e.g. Guided SAM).

**Understanding Situations**

Often there is explicit world knowledge about what has to be learned. To include such knowledge in the learning process, we study inductive logic programming (ILP), on top of deep learning models (e.g. object detection). Most information is probabilistic, e.g. objects are observed with some confidence. We extend ILP with probabilistic observations (Propper). Connecting logic to deep learning, we have developed methods that can do probabilistic logic inference, by means of neuro-symbolic programming. 

**Embodiment of AI**

With robots, one can do active perception: move to look better. With the rise of large AI models, we put CLIP on a robot. Robots typically learn shortcuts, which we mitigate by language-based augmentations, that are helpful for the vision to generalize better. For reasoning, we developed a dialogue between a language model (LLM) and a vision-language model (VLM). For instance, when encountering an obstacle, it decides to look for a metal box instead of any box, because a paper box is not strong enough to step on. During task planning, the robot may run into unknown settings, leading to errors. We devised a method to fix errors in a VLM efficiently on-the-job.

More details about my research activities and projects can be found in the Blog posts and Publications.

<img src="https://gertjanburghouts.github.io/pictures/college_cv_uva.jpg" width="80%">
