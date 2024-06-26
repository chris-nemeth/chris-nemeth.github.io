---
title: "Preferential Subsampling for Stochastic Gradient Langevin Dynamics"
collection: publications
permalink: /publication/2023-04-13-preferential-sgld
excerpt: ''
date: 2023-04-13
venue: 'AISTATS'
paperurl: 'https://proceedings.mlr.press/v206/putcha23a.html'
citation: 'Putcha, S., Nemeth, C. and Fearnhead, P., (2023). &quot;Preferential Subsampling for Stochastic Gradient Langevin Dynamics.&quot; <i>Proceedings of The 26th International Conference on Artificial Intelligence and Statistics</i>. PMLR 206:8837-8856, 2023.'
---
Stochastic gradient MCMC (SGMCMC) offers a scalable alternative to traditional MCMC, by constructing an unbiased estimate of the gradient of the log-posterior with a small, uniformly-weighted subsample of the data. While efficient to compute, the resulting gradient estimator may exhibit a high variance and impact sampler performance. The problem of variance control has been traditionally addressed by constructing a better stochastic gradient estimator, often using control variates. We propose to use a discrete, non-uniform probability distribution to preferentially subsample data points that have a greater impact on the stochastic gradient. In addition, we present a method of adaptively adjusting the subsample size at each iteration of the algorithm, so that we increase the subsample size in areas of the sample space where the gradient is harder to estimate. We demonstrate that such an approach can maintain the same level of accuracy while substantially reducing the average subsample size that is used.

[arXiv](https://arxiv.org/abs/2210.16189)
[Code](https://github.com/srshtiputcha/sgmcmc_preferential_subsampling)
