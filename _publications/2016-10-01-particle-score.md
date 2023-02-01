---
title: "Particle approximations of the score and observed information matrix for parameter estimation in state–space models with linear computational cost"
collection: publications
permalink: /publication/2016-10-01-particle-score
excerpt: ''
date: 2016-10-01
venue: 'Journal of Computational and Graphical Statistics'
paperurl: 'https://www.tandfonline.com/doi/abs/10.1080/10618600.2015.1093492'
citation: 'Nemeth, C., Fearnhead, P. and Mihaylova, L., (2016). &quot;Particle approximations of the score and observed information matrix for parameter estimation in state–space models with linear computational cost.&quot; <i>Journal of Computational and Graphical Statistics,</i> 25(4), pp.1138-1157.'
---
Poyiadjis, Doucet, and Singh showed how particle methods can be used to estimate both the score and the observed information matrix for state–space models. These methods either suffer from a computational cost that is quadratic in the number of particles, or produce estimates whose variance increases quadratically with the amount of data. This article introduces an alternative approach for estimating these terms at a computational cost that is linear in the number of particles. The method is derived using a combination of kernel density estimation, to avoid the particle degeneracy that causes the quadratically increasing variance, and Rao–Blackwellization. Crucially, we show the method is robust to the choice of bandwidth within the kernel density estimation, as it has good asymptotic properties regardless of this choice. Our estimates of the score and observed information matrix can be used within both online and batch procedures for estimating parameters for state–space models. Empirical results show improved parameter estimates compared to existing methods at a significantly reduced computational cost. Supplementary materials including code are available.

[arXiv](https://arxiv.org/abs/1306.0735)
