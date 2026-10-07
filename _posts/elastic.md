---
layout: post
title: "One Model, Every Size: Your Transformer Is Secretly Elastic"
date: 2026-10-07 06:00:00 -0000
categories: elastic transformer pruning efficiency on-edge
excerpt_separator: <!--more-->
---

AI models usually come in a few fixed sizes, like T-shirts: Small, Base, Large. You pick one based on your hardware and how fast you need answers, and then you're stuck with it. That works poorly in practice, because demand rarely stays constant. A model sized for a normal afternoon may buckle under a traffic spike, while a smaller model leaves performance unused when the servers are quiet. Ideally, a model would behave like a dimmer switch rather than a set of light bulbs: one model that can turn its compute up or down on the fly. In our new paper, we show that pre-trained transformers already contain this flexibility. You only need to know which parts to switch off first.

Our method ranks every building block of a transformer, meaning each individual neuron and each attention head, on a single common scale of importance. Once you have that ranking, you can shrink the model to any budget by removing units from the bottom of the list. The challenge is finding a good ranking, since units work together in ways that simple importance scores miss. We solve this with "soft pruning". Instead of deleting units outright during the search, we gradually dim them. This lets us use ordinary gradient descent to adjust the ranking until the model performs well across many budgets at once, from lightly trimmed to heavily pruned. The original weights are never touched: no retraining and no fine-tuning. Building an elastic model takes minutes, and the cost grows slower than the model's size.

The results are striking. We tested 27 vision and text models ranging from 22 million to 8 billion parameters. Performance degrades smoothly up to 60% sparsity, where existing pruning methods tend to collapse. Pruning the large DINOv3 vision model by half removes 427 million parameters, yet its ImageNet accuracy drops by only 0.8%. The savings also show up on real hardware. A pruned ViT-B/16 runs up to 1.8× faster on an A100 GPU, and switching between budgets takes less than half a millisecond. Two further findings stand out. For search and retrieval, slimmed-down query encoders stay compatible with an index built by the full model, so you can scale queries up or down without rebuilding anything. And within one model family, a pruned large model can beat a smaller model trained at full size. Decoder-based text embedders remain harder to prune deeply, which is a puzzle we are still working on. The broader lesson is encouraging: much of the model you already have is spare capacity you can use when you need it.

<img src="https://gertjanburghouts.github.io/pictures/elastic.jpg">
