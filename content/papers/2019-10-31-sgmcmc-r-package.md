---
title: "sgmcmc: An R package for stochastic gradient Markov chain Monte Carlo"
date: 2019-10-31
lastmod: 2019-10-31
tags: ["SGMCMC","stochastic gradient","R","Markov chain Monte Carlo"]
author: ["Jack Baker", "Paul Fearnhead", "Emily B Fox", "Christopher Nemeth"]
description: " "
summary: "Journal of Statistical Software"
editPost:
    URL: "https://www.jstatsoft.org/article/view/v091i03"
    Text: "Journal of Statistical Software"

---

---


##### Download

+ [Paper](https://www.jstatsoft.org/article/view/v091i03)
+ [arXiv](https://arxiv.org/abs/1710.00578)
+ [Code](https://github.com/STOR-i/sgmcmc)


---
##### Abstract

This paper introduces the R package sgmcmc; which can be used for Bayesian inference on problems with large datasets using stochastic gradient Markov chain Monte Carlo (SGMCMC). Traditional Markov chain Monte Carlo (MCMC) methods, such as Metropolis-Hastings, are known to run prohibitively slowly as the dataset size increases. SGMCMC solves this issue by only using a subset of data at each iteration. SGMCMC requires calculating gradients of the log likelihood and log priors, which can be time consuming and error prone to perform by hand. The sgmcmc package calculates these gradients itself using automatic differentiation, making the implementation of these methods much easier. To do this, the package uses the software library TensorFlow, which has a variety of statistical distributions and mathematical operations as standard, meaning a wide class of models can be built using this framework. SGMCMC has become widely adopted in the machine learning literature, but less so in the statistics community. We believe this may be partly due to lack of software; this package aims to bridge this gap.

---
##### Citation

Baker, J., Fearnhead, P., Fox, E.B. and Nemeth, C., 2019. sgmcmc: An R Package for Stochastic Gradient Markov Chain Monte Carlo. Journal of Statistical Software, 91, pp.1-27.

```BibTeX
@article{baker2019sgmcmc,
  title={sgmcmc: An R Package for Stochastic Gradient Markov Chain Monte Carlo},
  author={Baker, Jack and Fearnhead, Paul and Fox, Emily B and Nemeth, Christopher},
  journal={Journal of Statistical Software},
  volume={91},
  pages={1--27},
  year={2019}
}
```