---
title: "Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates"
collection: publications
permalink: /publication/2023-04-24-coin-sampling
excerpt: ''
date: 2023-04-24
venue: 'ICML'
paperurl: 'https://proceedings.mlr.press/v202/sharrock23a/sharrock23a.pdf'
citation: 'Sharrock, L. and Nemeth, C. (2023). &quot;Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates.&quot; <i>Proceedings of the 40th International Conference on Machine Learning.</i> PMLR 202:30850-30882.'
---

In recent years, particle-based variational inference (ParVI) methods such as Stein variational gradient descent (SVGD) have grown in popularity as scalable methods for Bayesian inference. Unfortunately, the properties of such methods invariably depend on hyperparameters such as the learning rate, which must be carefully tuned by the practitioner in order to ensure convergence to the target measure at a suitable rate. In this paper, we introduce a suite of new particle-based methods for scalable Bayesian inference based on coin betting, which are entirely learning-rate free. We illustrate the performance of our approach on a range of numerical examples, including several high-dimensional models and datasets, demonstrating comparable performance to other ParVI algorithms.

[arXiv](https://arxiv.org/abs/2301.11294)
[Code](https://github.com/louissharrock/Coin-SVGD)
