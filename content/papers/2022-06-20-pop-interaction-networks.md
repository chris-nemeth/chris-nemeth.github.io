---
title: "Modelling Populations of Interaction Networks via Distance Metrics"
date: 2025-07-09
lastmod: 2025-07-09
tags: ["network model","interaction network","distance metrics","Markov chain Monte Carlo","MCMC"]
author: ["George Bolt", "Simon Lunagomez","Christopher Nemeth"]
description: " "
summary: "Journal of Machine Learning Research (to appear)"
editPost:
    URL: "https://arxiv.org/abs/2206.09995"
    Text: "Journal of Machine Learning Research (to appear)"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2206.09995)


---
##### Abstract

Network data arises through observation of relational information between a collection of entities. Recent work in the literature has independently considered when (i) one observes a sample of networks, connectome data in neuroscience being a ubiquitous example, and (ii) the units of observation within a network are edges or paths, such as emails between people or a series of page visits to a website by a user, often referred to as interaction network data. The intersection of these two cases, however, is yet to be considered. In this paper, we propose a new Bayesian modelling framework to analyse such data. Given a practitioner-specified distance metric between observations, we define families of models through location and scale parameters, akin to a Gaussian distribution, with subsequent inference of model parameters providing reasoned statistical summaries for this non-standard data structure. To facilitate inference, we propose specialised Markov chain Monte Carlo (MCMC) schemes capable of sampling from doubly-intractable posterior distributions over discrete and multi-dimensional parameter spaces. Through simulation studies we confirm the efficacy of our methodology and inference scheme, whilst its application we illustrate via an example analysis of a location-based social network (LSBN) data set.


---
##### Citation

Bolt, G., Lunagomez, S. and Nemeth, C., 2025. Modelling Populations of Interaction Networks via Distance Metrics. *Journal of Machine Learning Research (to appear)*.

```BibTeX
@article{bolt2025modelling,
  title={Modelling Populations of Interaction Networks via Distance Metrics},
  author={Bolt, George and Lunag{\'o}mez, Sim{\'o}n and Nemeth, Christopher},
  journal={Journal of Machine Learning Research (to appear)},
  year={2025}
}
```