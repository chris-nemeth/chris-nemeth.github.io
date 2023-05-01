---
title: "Transport Elliptical Slice Sampling"
collection: publications
permalink: /publication/2024-04-13-transport-ess
excerpt: ''
date: 2023-04-13
venue: 'AISTATS'
paperurl: 'https://proceedings.mlr.press/v206/cabezas23a.html'
citation: 'Cabezas, A. and Nemeth, C., (2023). &quot;Transport Elliptical Slice Sampling.&quot; <i>Proceedings of The 26th International Conference on Artificial Intelligence and Statistics.</i>PMLR 206:3664-3676, 2023.'
---
We introduce a new framework for efficient sampling from complex probability distributions, using a combination of normalizing flows and elliptical slice sampling (Murray et al., 2010). The core idea is to learn a diffeomorphism, via normalizing flows, that maps the non-Gaussian structure of our target distribution to an approximately Gaussian distribution. We can then sample from our transformed distribution using the elliptical slice sampler, which is an efficient and tuning-free Markov chain Monte Carlo (MCMC) algorithm. The samples are then pulled back using an inverse normalizing flow to yield samples which approximate the stationary target distribution of interest. Our transformed elliptical slice sampler (TESS) is efficiently designed for modern computer architectures, where its adaptation mechanism utilizes parallel cores to rapidly run multiple Markov chains for only a few iterations. Numerical demonstrations show that TESS produce Monte Carlo samples from the target distribution with lower autocorrelation compared to non-transformed samplers. Additionally, assuming a sufficiently flexible diffeomorphism, TESS demonstrates significant improvements in efficiency when compared to gradient-based proposals designed to run on parallel computer architectures.

[arXiv](https://arxiv.org/abs/2210.10644)
