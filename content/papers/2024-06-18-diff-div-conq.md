---
title: "Diffusion Generative Modelling for Divide-and-Conquer MCMC"
date: 2024-06-18
lastmod: 2024-06-18
tags: ["Markov chain Monte Carlo","MCMC","divide and conquer", "diffusion models"]
author: ["Connie Trojan","Paul Fearnhead","Christopher Nemeth"]
description: " "
summary: "arXiv preprint"
editPost:
    URL: "https://arxiv.org/abs/2406.11664"
    Text: "arXiv preprint"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2406.11664)
+ [Code](https://github.com/ctrojan/DiffusionDnC)

---
##### Abstract

Divide-and-conquer MCMC is a strategy for parallelising Markov Chain Monte Carlo sampling by running independent samplers on disjoint subsets of a dataset and merging their output. An ongoing challenge in the literature is to efficiently perform this merging without imposing distributional assumptions on the posteriors. We propose using diffusion generative modelling to fit density approximations to the subposterior distributions. This approach outperforms existing methods on challenging merging problems, while its computational cost scales more efficiently to high dimensional problems than existing density estimation approaches.

---
##### Citation

Trojan, C., Fearnhead, P., and Nemeth, C. (2024). Diffusion Generative Modelling for Divide-and-Conquer MCMC. *arXiv preprint*.

```BibTeX
@article{trojan2024diffusion,
  title={Diffusion Generative Modelling for Divide-and-Conquer MCMC},
  author={Trojan, Connie and Fearnhead, Paul and Nemeth, Christopher},
  journal={arXiv preprint arXiv:2406.11664},
  year={2024}
}
```