---
title: "Stochastic Gradient Markov Chain Monte Carlo"
collection: publications
permalink: /publication/2021-01-04-sgmcmc-review
excerpt: ''
date: 2021-01-04
venue: 'Journal of the American Statistical Association'
paperurl: 'https://www.tandfonline.com/doi/full/10.1080/01621459.2020.1847120'
citation: 'Nemeth, C. and Fearnhead, P., (2021). &quot;Stochastic gradient markov chain monte carlo.&quot; <i>Journal of the American Statistical Association,</i> 116(533), pp.433-450.'
---

Markov chain Monte Carlo (MCMC) algorithms are generally regarded as the gold standard technique for Bayesian inference. They are theoretically well-understood and conceptually simple to apply in practice. The drawback of MCMC is that performing exact inference generally requires all of the data to be processed at each iteration of the algorithm. For large datasets, the computational cost of MCMC can be prohibitive, which has led to recent developments in scalable Monte Carlo algorithms that have a significantly lower computational cost than standard MCMC. In this article, we focus on a particular class of scalable Monte Carlo algorithms, stochastic gradient Markov chain Monte Carlo (SGMCMC) which utilizes data subsampling techniques to reduce the per-iteration cost of MCMC. We provide an introduction to some popular SGMCMC algorithms and review the supporting theoretical results, as well as comparing the efficiency of SGMCMC algorithms against MCMC on benchmark examples. 

[arXiv](https://arxiv.org/abs/2002.00033)
[code](https://github.com/chris-nemeth/sgmcmc-review-paper)
