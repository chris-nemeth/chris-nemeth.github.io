---
title: "Preferential Subsampling for Stochastic Gradient Langevin Dynamics"
date: 2023-04-13
lastmod: 2023-04-13
tags: ["stochastic gradient Langevin dynamics","SGLD","preferential subsampling"]
author: ["Srshti Putcha","Christopher Nemeth","Paul Fearnhead"]
description: " "
summary: "International Conference on Artificial Intelligence and Statistics (AISTATS)"
editPost:
    URL: "https://proceedings.mlr.press/v206/putcha23a.html"
    Text: "AISTATS 2023"

---

---


##### Download

+ [Paper](https://proceedings.mlr.press/v206/putcha23a/putcha23a.pdf)
+ [arXiv](https://arxiv.org/abs/2210.16189)
+ [Code](https://github.com/srshtiputcha/sgmcmc_preferential_subsampling)


---
##### Abstract
Stochastic gradient MCMC (SGMCMC) offers a scalable alternative to traditional MCMC, by constructing an unbiased estimate of the gradient of the log-posterior with a small, uniformly-weighted subsample of the data. While efficient to compute, the resulting gradient estimator may exhibit a high variance and impact sampler performance. The problem of variance control has been traditionally addressed by constructing a better stochastic gradient estimator, often using control variates. We propose to use a discrete, non-uniform probability distribution to preferentially subsample data points that have a greater impact on the stochastic gradient. In addition, we present a method of adaptively adjusting the subsample size at each iteration of the algorithm, so that we increase the subsample size in areas of the sample space where the gradient is harder to estimate. We demonstrate that such an approach can maintain the same level of accuracy while substantially reducing the average subsample size that is used.



---
##### Citation


Putcha, S., Nemeth, C. and Fearnhead, P., 2023, April. Preferential Subsampling for Stochastic Gradient Langevin Dynamics. In International Conference on Artificial Intelligence and Statistics (pp. 8837-8856). PMLR.

```BibTeX
@inproceedings{putcha2023preferential,
  title={Preferential Subsampling for Stochastic Gradient Langevin Dynamics},
  author={Putcha, Srshti and Nemeth, Christopher and Fearnhead, Paul},
  booktitle={International Conference on Artificial Intelligence and Statistics},
  pages={8837--8856},
  year={2023},
  organization={PMLR}
}
```
