---
title: "Merging MCMC Subposteriors through Gaussian-Process Approximations"
date: 2018-06-01
lastmod: 2019-06-01
tags: ["Markov chain Monte Carlo","MCMC","Gaussian processes","subposteriors","divide-and-conquer"]
author: ["Christopher Nemeth","Chris Sherlock"]
description: " "
summary: "Bayesian Analysis"
editPost:
    URL: "https://projecteuclid.org/journals/bayesian-analysis/volume-13/issue-2/Merging-MCMC-Subposteriors-through-Gaussian-Process-Approximations/10.1214/17-BA1063.full"
    Text: "Bayesian Analysis"

---

---


##### Download

+ [Paper](https://projecteuclid.org/journals/bayesian-analysis/volume-13/issue-2/Merging-MCMC-Subposteriors-through-Gaussian-Process-Approximations/10.1214/17-BA1063.full)
+ [arXiv](https://arxiv.org/abs/1605.08576)
 

---
##### Abstract

Markov chain Monte Carlo (MCMC) algorithms have become powerful tools for Bayesian inference. However, they do not scale well to large-data problems. Divide-and-conquer strategies, which split the data into batches and, for each batch, run independent MCMC algorithms targeting the corresponding subposterior, can spread the computational burden across a number of separate computer cores. The challenge with such strategies is in recombining the subposteriors to approximate the full posterior. By creating a Gaussian-process approximation for each log-subposterior density we create a tractable approximation for the full posterior. This approximation is exploited through three methodologies: firstly a Hamiltonian Monte Carlo algorithm targeting the expectation of the posterior density provides a sample from an approximation to the posterior; secondly, evaluating the true posterior at the sampled points leads to an importance sampler that, asymptotically, targets the true posterior expectations; finally, an alternative importance sampler uses the full Gaussian-process distribution of the approximation to the log-posterior density to re-weight any initial sample and provide both an estimate of the posterior expectation and a measure of the uncertainty in it.

---
##### Citation

Nemeth, C. and Sherlock, C., 2018. Merging MCMC Subposteriors through Gaussian-Process Approximations. Bayesian Analysis, 13(2), pp.507-530.

```BibTeX
@article{nemeth2018merging,
  title={Merging MCMC Subposteriors through Gaussian-Process Approximations},
  author={Nemeth, Christopher and Sherlock, Chris},
  journal={Bayesian Analysis},
  volume={13},
  number={2},
  pages={507--530},
  year={2018}
}
```