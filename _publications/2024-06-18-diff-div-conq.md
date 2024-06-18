---
title: "Diffusion Generative Modelling for Divide-and-Conquer MCMC"
collection: publications
permalink: /publication/2024-06-18-diff-div-conq
excerpt: ''
date: 2024-06-18
venue: 'arXiv preprint'
paperurl: 'https://arxiv.org/abs/2406.11664'
citation: 'Trojan, C., Fearnhead, P., and Nemeth, C. (2024). &quot; Diffusion Generative Modelling for Divide-and-Conquer MCMC &quot; <i>arXiv preprint.</i>.'
---
Divide-and-conquer MCMC is a strategy for parallelising Markov Chain Monte Carlo sampling by running independent samplers on disjoint subsets of a dataset and merging their output. An ongoing challenge in the literature is to efficiently perform this merging without imposing distributional assumptions on the posteriors. We propose using diffusion generative modelling to fit density approximations to the subposterior distributions. This approach outperforms existing methods on challenging merging problems, while its computational cost scales more efficiently to high dimensional problems than existing density estimation approaches.

[arXiv](https://arxiv.org/abs/2406.11664)
[Code](https://github.com/ctrojan/DiffusionDnC)
