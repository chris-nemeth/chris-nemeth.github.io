---
title: "Transport Elliptical Slice Sampling"
date: 2023-04-13
lastmod: 2023-04-13
tags: ["elliptical slice sampling","normalizing flow","Bayesian inference"]
author: ["Alberto Cabezas","Christopher Nemeth"]
description: " "
summary: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
editPost:
    URL: "https://proceedings.mlr.press/v206/cabezas23a.html"
    Text: "AISTATS 2023"

---

---


##### Download

+ [Paper](https://proceedings.mlr.press/v206/cabezas23a/cabezas23a.pdf)
+ [arXiv](https://arxiv.org/abs/2210.10644)
+ [Code](https://github.com/albcab/TESS)


---
##### Abstract

We introduce a new framework for efficient sampling from complex probability distributions, using a combination of normalizing flows and elliptical slice sampling (Murray et al., 2010). The core idea is to learn a diffeomorphism, via normalizing flows, that maps the non-Gaussian structure of our target distribution to an approximately Gaussian distribution. We can then sample from our transformed distribution using the elliptical slice sampler, which is an efficient and tuning-free Markov chain Monte Carlo (MCMC) algorithm. The samples are then pulled back using an inverse normalizing flow to yield samples which approximate the stationary target distribution of interest. Our transformed elliptical slice sampler (TESS) is efficiently designed for modern computer architectures, where its adaptation mechanism utilizes parallel cores to rapidly run multiple Markov chains for only a few iterations. Numerical demonstrations show that TESS produce Monte Carlo samples from the target distribution with lower autocorrelation compared to non-transformed samplers. Additionally, assuming a sufficiently flexible diffeomorphism, TESS demonstrates significant improvements in efficiency when compared to gradient-based proposals designed to run on parallel computer architectures.

---
##### Citation


Cabezas, A. and Nemeth, C., 2023. Transport elliptical slice sampling. In *International Conference on Artificial Intelligence and Statistics* (pp. 3664-3676). PMLR.

```BibTeX
@inproceedings{cabezas2023transport,
  title={Transport elliptical slice sampling},
  author={Cabezas, Alberto and Nemeth, Christopher},
  booktitle={International Conference on Artificial Intelligence and Statistics},
  pages={3664--3676},
  year={2023},
  organization={PMLR}
}
```

