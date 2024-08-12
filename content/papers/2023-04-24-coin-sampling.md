---
title: "Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates"
date: 2023-07-24
lastmod: 2023-07-24
tags: ["learning-rate-free","Bayesian inference","coin sampling","particle variational inference","SVGD"]
author: ["Louis Sharrock","Christopher Nemeth"]
description: " "
summary: "International Conference on Machine Learning (ICML)"
editPost:
    URL: "https://proceedings.mlr.press/v202/sharrock23a"
    Text: "ICML 2023"

---

---


##### Download

+ [Paper](https://proceedings.mlr.press/v202/sharrock23a/sharrock23a.pdf)
+ [arXiv](https://arxiv.org/abs/2301.11294)
+ [Code](https://github.com/louissharrock/Coin-SVGD)
  

---
##### Abstract

In recent years, particle-based variational inference (ParVI) methods such as Stein variational gradient descent (SVGD) have grown in popularity as scalable methods for Bayesian inference. Unfortunately, the properties of such methods invariably depend on hyperparameters such as the learning rate, which must be carefully tuned by the practitioner in order to ensure convergence to the target measure at a suitable rate. In this paper, we introduce a suite of new particle-based methods for scalable Bayesian inference based on coin betting, which are entirely learning-rate free. We illustrate the performance of our approach on a range of numerical examples, including several high-dimensional models and datasets, demonstrating comparable performance to other ParVI algorithms.

---
##### Citation

Sharrock, L. and Nemeth, C., 2023. Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates. In *International Conference on Machine Learning* (pp. 30850-30882). PMLR.

```BibTeX
@inproceedings{sharrock2023coin,
  title={Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates},
  author={Sharrock, Louis and Nemeth, Christopher},
  booktitle={International Conference on Machine Learning},
  pages={30850--30882},
  year={2023},
  organization={PMLR}
}
```