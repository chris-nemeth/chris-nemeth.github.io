---
title: "Learning Rate Free Sampling in Constrained Domains"
date: 2023-11-02
lastmod: 2024-08-10
tags: ["learning-rate-free","particle variational inference","mirror descent","constrained sampling"]
author: ["Louis Sharrock","Lester Mackey","Christopher Nemeth"]
description: " "
summary: "Neural Information Processing Systems (NeurIPS)"
editPost:
    URL: "https://openreview.net/forum?id=TNAGFUcSP7"
    Text: "NeurIPS 2023"

---

---


##### Download

+ [Paper](https://openreview.net/forum?id=TNAGFUcSP7)
+ [arXiv](https://arxiv.org/abs/2305.14943)
+ [Code](https://github.com/louissharrock/constrained-coin-sampling)



---
##### Abstract

We introduce a suite of new particle-based algorithms for sampling on constrained domains which are entirely learning rate free. Our approach leverages coin betting ideas from convex optimisation, and the viewpoint of constrained sampling as a mirrored optimisation problem on the space of probability measures. Based on this viewpoint, we also introduce a unifying framework for several existing constrained sampling algorithms, including mirrored Langevin dynamics and mirrored Stein variational gradient descent. We demonstrate the performance of our algorithms on a range of numerical examples, including sampling from targets on the simplex, sampling with fairness constraints, and constrained sampling problems in post-selection inference. Our results indicate that our algorithms achieve competitive performance with existing constrained sampling methods, without the need to tune any hyperparameters.

---
##### Citation

Sharrock, L., Mackey, L. and Nemeth, C. (2023). Learning Rate Free Sampling in Constrained Domains. *Advances in Neural Information Processing Systems (NeurIPS)*. Vol. 36, p. 65380-65415.

```BibTeX
@article{sharrock2023learning,
  title={Learning rate free sampling in constrained domains},
  author={Sharrock, Louis and Mackey, Lester and Nemeth, Christopher},
  journal={Advances in Neural Information Processing Systems},
  volume={36},
  pages={65380--65415},
  year={2023}
}
```
