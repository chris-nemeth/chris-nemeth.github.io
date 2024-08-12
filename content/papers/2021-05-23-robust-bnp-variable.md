---
title: "Robust Bayesian Nonparametric Variable Selection for Linear Regression"
date: 2024-05-24
lastmod: 2024-05-24
tags: ["Markov chain Monte Carlo","MCMC","robust regression","variable selection"]
author: ["Alberto Cabezas","Marco Battiston","Christopher Nemeth"]
description: " "
summary: "Stat"
editPost:
    URL: "https://onlinelibrary.wiley.com/doi/full/10.1002/sta4.696"
    Text: "Stat"

---

---


##### Download

+ [Paper](https://onlinelibrary.wiley.com/doi/full/10.1002/sta4.696)
+ [arXiv](https://arxiv.org/abs/2105.11022)
+ [Code](https://github.com/albcab/RobustVariableSelection)

---
##### Abstract

Spike-and-slab and horseshoe regression are arguably the most popular Bayesian variable selection approaches for linear regression models. However, their performance can deteriorate if outliers and heteroskedasticity are present in the data, which are common features in many real-world statistics and machine learning applications. In this work, we propose a Bayesian nonparametric approach to linear regression that performs variable selection while accounting for outliers and heteroskedasticity. Our proposed model is an instance of a Dirichlet process scale mixture model with the advantage that we can derive the full conditional distributions of all parameters in closed form, hence producing an efficient Gibbs sampler for posterior inference. Moreover, we present how to extend the model to account for heavy-tailed response variables. The performance of the model is tested against competing algorithms on synthetic and real-world datasets.


---
##### Citation

Cabezas, A., Battiston, M. and Nemeth, C., 2024. Robust Bayesian nonparametric variable selection for linear regression. Stat, 13(2), p.e696.

```BibTeX
@article{cabezas2024robust,
  title={Robust Bayesian nonparametric variable selection for linear regression},
  author={Cabezas, Alberto and Battiston, Marco and Nemeth, Christopher},
  journal={Stat},
  volume={13},
  number={2},
  pages={e696},
  year={2024},
  publisher={Wiley Online Library}
}
```