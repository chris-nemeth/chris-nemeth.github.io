---
title: "Learning Rate Free Sampling in Constrained Domains"
collection: publications
permalink: /publication/2023-05-25-mirror-coin
excerpt: ''
date: 2023-09-21
venue: 'NeurIPS'
paperurl: 'https://openreview.net/forum?id=TNAGFUcSP7'
citation: 'Sharrock, L., Mackey, L. and Nemeth, C. (2023). &quot;Learning Rate Free Sampling in Constrained Domains&quot; <i>NeurIPS 2023.</i>.'
---

We introduce a suite of new particle-based algorithms for sampling on constrained domains which are entirely learning rate free. Our approach leverages coin betting ideas from convex optimisation, and the viewpoint of constrained sampling as a mirrored optimisation problem on the space of probability measures. Based on this viewpoint, we also introduce a unifying framework for several existing constrained sampling algorithms, including mirrored Langevin dynamics and mirrored Stein variational gradient descent. We demonstrate the performance of our algorithms on a range of numerical examples, including sampling from targets on the simplex, sampling with fairness constraints, and constrained sampling problems in post-selection inference. Our results indicate that our algorithms achieve competitive performance with existing constrained sampling methods, without the need to tune any hyperparameters.

[arXiv](https://arxiv.org/abs/2305.14943)
[Code](https://github.com/louissharrock/constrained-coin-sampling)
