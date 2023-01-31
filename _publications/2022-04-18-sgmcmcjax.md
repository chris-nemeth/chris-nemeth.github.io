---
title: "SGMCMCJax: a lightweight JAX library for stochastic gradient Markov chain Monte Carlo algorithms"
collection: publications
permalink: /publication/2022-04-18-sgmcmcjax
excerpt: ''
date: 2022-04-18
venue: 'Journal of Open Source Software'
paperurl: 'https://joss.theoj.org/papers/10.21105/joss.04113.pdf'
citation: 'Coullon, J. and Nemeth, C., (2022). &quot;SGMCMCJax: a lightweight JAX library for stochastic gradient Markov chain Monte Carlo algorithms.&quot; <i>Journal of Open Source Software,</i> 7(72), p.4113.'
---
In Bayesian inference, the posterior distribution is the probability distribution over the model parameters resulting from the prior distribution and the likelihood. One can compute integrals over this distribution to obtain quantities of interest, such as the posterior mean and variance, or credible uncertainty regions. However, as these integrals are often intractable for problems of interest they require numerical methods to approximate them.

Markov Chain Monte Carlo (MCMC) is currently the gold standard for approximating integrals needed in Bayesian inference. However, as these algorithms become prohibitively expensive for large datasets, stochastic gradient MCMC (SGMCMC)(Ma et al., 2015; Nemeth & Fearnhead, 2021) is a popular approach to approximate these integrals in these cases. This class of scalable algorithms uses data subsampling techniques to approximate gradient based sampling algorithms, and are regularly used to fit statistical models or Bayesian neural networks (BNNs). The SGMCMC literature develops new algorithms by finding novel gradient estimation techniques, designing more efficient diffusions, and finding more stable numerical discretisations to these diffusions. SGMCMCJax is a lightweight library that is designed to allow the user to innovate along these lines or use one of the existing gradient-based SGMCMC algorithms already included in the library. This makes SGMCMCJax very well suited for both research purposes and practical applications.

[Code](https://github.com/jeremiecoullon/SGMCMCJax)
