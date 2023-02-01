---
title: "Merging MCMC Subposteriors through Gaussian-Process Approximations"
collection: publications
permalink: /publication/2018-06-01-merging-mcmc-gp
excerpt: ''
date: 2018-06-01
venue: 'Bayesian Analysis'
paperurl: 'https://projecteuclid.org/journals/bayesian-analysis/volume-13/issue-2/Merging-MCMC-Subposteriors-through-Gaussian-Process-Approximations/10.1214/17-BA1063.full'
citation: 'Nemeth, C. and Sherlock, C. &quot;Merging MCMC Subposteriors through Gaussian-Process Approximations.&quot; <i>Bayesian Analysis</i>. 13 (2) 507 - 530.'
---
Markov chain Monte Carlo (MCMC) algorithms have become powerful tools for Bayesian inference. However, they do not scale well to large-data problems. Divide-and-conquer strategies, which split the data into batches and, for each batch, run independent MCMC algorithms targeting the corresponding subposterior, can spread the computational burden across a number of separate computer cores. The challenge with such strategies is in recombining the subposteriors to approximate the full posterior. By creating a Gaussian-process approximation for each log-subposterior density we create a tractable approximation for the full posterior. This approximation is exploited through three methodologies: firstly a Hamiltonian Monte Carlo algorithm targeting the expectation of the posterior density provides a sample from an approximation to the posterior; secondly, evaluating the true posterior at the sampled points leads to an importance sampler that, asymptotically, targets the true posterior expectations; finally, an alternative importance sampler uses the full Gaussian-process distribution of the approximation to the log-posterior density to re-weight any initial sample and provide both an estimate of the posterior expectation and a measure of the uncertainty in it.

[arXiv](https://arxiv.org/abs/1605.08576)
