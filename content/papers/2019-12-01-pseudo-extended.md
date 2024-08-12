---
title: "Pseudo-extended Markov chain Monte Carlo"
date: 2019-12-01
lastmod: 2019-12-01
tags: ["Markov chain Monte Carlo","MCMC","multi-modal distributions"]
author: ["Christopher Nemeth", "Fredrik Lindsten", "Maurizio Filippone", "James Hensman"]
description: " "
summary: "Neural Information Processing Systems (NeurIPS)"
editPost:
    URL: "https://proceedings.neurips.cc/paper/2019/hash/e3ca0449fa2ea7701a7ac53fb719c51a-Abstract.html"
    Text: "NeurIPS 2019"

---

---


##### Download

+ [Paper](https://proceedings.neurips.cc/paper/2019/hash/e3ca0449fa2ea7701a7ac53fb719c51a-Abstract.html)
+ [arXiv](https://arxiv.org/abs/1708.05239)
+ [Code](https://github.com/chris-nemeth/pseudo-extended-mcmc-code)


---
##### Abstract

Sampling from posterior distributions using Markov chain Monte Carlo (MCMC) methods can require an exhaustive number of iterations, particularly when the posterior is multi-modal as the MCMC sampler can become trapped in a local mode for a large number of iterations. In this paper, we introduce the pseudo-extended MCMC method as a simple approach for improving the mixing of the MCMC sampler for multi-modal posterior distributions. The pseudo-extended method augments the state-space of the posterior using pseudo-samples as auxiliary variables. On the extended space, the modes of the posterior are connected, which allows the MCMC sampler to easily move between well-separated posterior modes. We demonstrate that the pseudo-extended approach delivers improved MCMC sampling over the Hamiltonian Monte Carlo algorithm on multi-modal posteriors, including Boltzmann machines and models with sparsity-inducing priors.


---
##### Citation

Nemeth, C., Lindsten, F., Filippone, M. and Hensman, J., 2019. Pseudo-extended markov chain monte carlo. Advances in Neural Information Processing Systems, 32.

```BibTeX
@article{nemeth2019pseudo,
  title={Pseudo-extended markov chain monte carlo},
  author={Nemeth, Christopher and Lindsten, Fredrik and Filippone, Maurizio and Hensman, James},
  journal={Advances in Neural Information Processing Systems},
  volume={32},
  year={2019}
}
```