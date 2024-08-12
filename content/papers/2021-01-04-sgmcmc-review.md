---
title: "Stochastic Gradient Markov Chain Monte Carlo"
date: 2021-01-04
lastmod: 2021-01-04
tags: ["Markov chain Monte Carlo","Bayesian inference","MCMC","SGMCMC","stochastic gradient"]
author: ["Christopher Nemeth","Paul Fearnhead"]
description: " "
summary: "Journal of the American Statistical Association"
editPost:
    URL: "https://www.tandfonline.com/doi/full/10.1080/01621459.2020.1847120"
    Text: "Journal of the American Statistical Association"

---

---


##### Download

+ [Paper](https://www.tandfonline.com/doi/full/10.1080/01621459.2020.1847120)
+ [arXiv](https://arxiv.org/abs/2002.00033)
+ [Code](https://github.com/chris-nemeth/sgmcmc-review-paper)



---
##### Abstract

Markov chain Monte Carlo (MCMC) algorithms are generally regarded as the gold standard technique for Bayesian inference. They are theoretically well-understood and conceptually simple to apply in practice. The drawback of MCMC is that performing exact inference generally requires all of the data to be processed at each iteration of the algorithm. For large datasets, the computational cost of MCMC can be prohibitive, which has led to recent developments in scalable Monte Carlo algorithms that have a significantly lower computational cost than standard MCMC. In this article, we focus on a particular class of scalable Monte Carlo algorithms, stochastic gradient Markov chain Monte Carlo (SGMCMC) which utilizes data subsampling techniques to reduce the per-iteration cost of MCMC. We provide an introduction to some popular SGMCMC algorithms and review the supporting theoretical results, as well as comparing the efficiency of SGMCMC algorithms against MCMC on benchmark examples. 


---
##### Citation

Nemeth, C. and Fearnhead, P., 2021. Stochastic gradient markov chain monte carlo. Journal of the American Statistical Association, 116(533), pp.433-450.

```BibTeX
@article{nemeth2021stochastic,
  title={Stochastic gradient markov chain monte carlo},
  author={Nemeth, Christopher and Fearnhead, Paul},
  journal={Journal of the American Statistical Association},
  volume={116},
  number={533},
  pages={433--450},
  year={2021},
  publisher={Taylor \& Francis}
}
```