---
title: "Particle approximations of the score and observed information matrix for parameter estimation in state–space models with linear computational cost"
date: 2016-10-01
lastmod: 2016-10-01
tags: ["sequential Monte Carlo","state-space models","SMC","particle filters"]
author: ["Christopher Nemeth", "Paul Fearnhead","Lyudmila Mihaylova"]
description: " "
summary: "Journal of Computational and Graphical Statistics"
editPost:
    URL: "https://www.tandfonline.com/doi/abs/10.1080/10618600.2015.1093492"
    Text: "Journal of Computational and Graphical Statistics"

---

---


##### Download

+ [Paper](https://www.tandfonline.com/doi/abs/10.1080/10618600.2015.1093492)
+ [arXiv](https://arxiv.org/abs/1306.0735)


---
##### Abstract

Poyiadjis, Doucet, and Singh showed how particle methods can be used to estimate both the score and the observed information matrix for state–space models. These methods either suffer from a computational cost that is quadratic in the number of particles, or produce estimates whose variance increases quadratically with the amount of data. This article introduces an alternative approach for estimating these terms at a computational cost that is linear in the number of particles. The method is derived using a combination of kernel density estimation, to avoid the particle degeneracy that causes the quadratically increasing variance, and Rao–Blackwellization. Crucially, we show the method is robust to the choice of bandwidth within the kernel density estimation, as it has good asymptotic properties regardless of this choice. Our estimates of the score and observed information matrix can be used within both online and batch procedures for estimating parameters for state–space models. Empirical results show improved parameter estimates compared to existing methods at a significantly reduced computational cost. Supplementary materials including code are available.


---
##### Citation

Nemeth, C., Fearnhead, P. and Mihaylova, L., 2016. Particle approximations of the score and observed information matrix for parameter estimation in state–space models with linear computational cost. Journal of Computational and Graphical Statistics, 25(4), pp.1138-1157.

```BibTeX
@article{nemeth2016particle,
  title={Particle approximations of the score and observed information matrix for parameter estimation in state--space models with linear computational cost},
  author={Nemeth, Christopher and Fearnhead, Paul and Mihaylova, Lyudmila},
  journal={Journal of Computational and Graphical Statistics},
  volume={25},
  number={4},
  pages={1138--1157},
  year={2016},
  publisher={Taylor \& Francis}
}
```