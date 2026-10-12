---
title: "Spatial Prediction with Guided Diffusion"
date: 2026-10-09
lastmod: 2026-10-09
tags: ["spatial statistics","diffusion models","guided diffusion","spatial prediction"]
author: ["Andrew Zammit-Mangion","Lachlan Astfalck","Raphaël Huser","Christopher Nemeth","Henry Moss"]
description: " "
summary: "arXiv preprint"
editPost:
    URL: "https://arxiv.org/abs/2610.12967"
    Text: "arXiv preprint"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2610.12967)


---
##### Abstract

Spatial prediction is a critically important task in data analyses that involve spatially or spatio-temporally-referenced data. It is commonly carried out using hierarchical models, which comprise a process model describing the latent process of interest, and a data model describing how the process is observed. The target quantity is the predictive distribution, which is the conditional distribution of the latent spatial process given the observed data. Unfortunately, the predictive distribution is rarely available in closed form and can be difficult to sample from. Here, we show how recent developments in guided diffusion modelling from machine learning can address a wide class of problems in spatial prediction when the likelihood function derived from the data model is known and differentiable, possibly after relaxation. To show the versatility of the approach, we apply it to both Gaussian and non-Gaussian process models and a variety of data models that describe direct partial observations, linear and areal aggregates, counts, right censoring, and area-exceedance functionals. Where possible, we validate the framework against exact and Markov-chain-Monte-Carlo (MCMC)-derived predictive distributions. We demonstrate our approach on several simulation studies and in a controlled experiment of methane-flux inversion over the UK and Ireland. We show that guided diffusion can sample from the correct predictive distribution in a variety of settings, that it can be applied to models where MCMC is intractable, and that it scales well with the dimensionality of the latent process.

---
##### Citation

Zammit-Mangion, A., Astfalck, L., Huser, R., Nemeth, C. and Moss, H. (2026). Spatial Prediction with Guided Diffusion. *arXiv preprint*.

```BibTeX
@article{zammitmangion2026spatial,
  title={Spatial Prediction with Guided Diffusion},
  author={Zammit-Mangion, Andrew and Astfalck, Lachlan and Huser, Rapha{\"e}l and Nemeth, Christopher and Moss, Henry},
  journal={arXiv preprint arXiv:2610.12967},
  year={2026}
}
```
