---
title: "Efficient and generalizable tuning strategies for stochastic gradient MCMC"
collection: publications
permalink: /publication/2023-04-04-tuning-sgmcmc
excerpt: ''
date: 2023-04-04
venue: 'Statistics and Computing'
paperurl: 'https://link.springer.com/article/10.1007/s11222-023-10233-3'
citation: 'Coullon, J., South, L. and Nemeth, C., (2023). &quot;Efficient and generalizable tuning strategies for stochastic gradient MCMC.&quot; <i>Statistics and Computing.</i> 33(66).'
---
Stochastic gradient Markov chain Monte Carlo (SGMCMC) is a popular class of algorithms for scalable Bayesian inference. However, these algorithms include hyperparameters such as step size or batch size that influence the accuracy of estimators based on the obtained posterior samples. As a result, these hyperparameters must be tuned by the practitioner and currently no principled and automated way to tune them exists. Standard MCMC tuning methods based on acceptance rates cannot be used for SGMCMC, thus requiring alternative tools and diagnostics. We propose a novel bandit-based algorithm that tunes the SGMCMC hyperparameters by minimizing the Stein discrepancy between the true posterior and its Monte Carlo approximation. We provide theoretical results supporting this approach and assess various Stein-based discrepancies. We support our results with experiments on both simulated and real datasets, and find that this method is practical for a wide range of applications.

[arXiv](https://arxiv.org/abs/2105.13059)
[Code](https://github.com/jeremiecoullon/SGMCMC_bandit_tuning)
