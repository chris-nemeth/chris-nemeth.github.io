---
title: "sgmcmc: An R package for stochastic gradient Markov chain Monte Carlo"
collection: publications
permalink: /publication/2019-10-31-sgmcmc-r-package
excerpt: ''
date: 2019-10-31
venue: 'Journal of Statistical Software'
paperurl: 'https://www.jstatsoft.org/article/view/v091i03'
citation: 'Baker, J., Fearnhead, P., Fox, E. B., & Nemeth, C. (2019). &quot;sgmcmc: An R Package for Stochastic Gradient Markov Chain Monte Carlo.&quot; <i>Journal of Statistical Software,</i> 91(3), 1–27.'
---
This paper introduces the R package sgmcmc; which can be used for Bayesian inference on problems with large datasets using stochastic gradient Markov chain Monte Carlo (SGMCMC). Traditional Markov chain Monte Carlo (MCMC) methods, such as Metropolis-Hastings, are known to run prohibitively slowly as the dataset size increases. SGMCMC solves this issue by only using a subset of data at each iteration. SGMCMC requires calculating gradients of the log likelihood and log priors, which can be time consuming and error prone to perform by hand. The sgmcmc package calculates these gradients itself using automatic differentiation, making the implementation of these methods much easier. To do this, the package uses the software library TensorFlow, which has a variety of statistical distributions and mathematical operations as standard, meaning a wide class of models can be built using this framework. SGMCMC has become widely adopted in the machine learning literature, but less so in the statistics community. We believe this may be partly due to lack of software; this package aims to bridge this gap.

[arXiv](https://arxiv.org/abs/1710.00578)
[code](https://github.com/STOR-i/sgmcmc)
