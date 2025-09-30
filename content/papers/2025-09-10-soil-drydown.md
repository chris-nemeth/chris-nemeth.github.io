---
title: "Inferring Soil Drydown Behaviour with Adaptive Bayesian Online Changepoint Analysis"
date: 2025-09-10
lastmod: 2025-09-10
tags: ["changepoints","soil","time series"]
author: ["Mengyi Gong","Christopher Nemeth","Rebecca Killick","Peter Strauss","John Quinton"]
description: " "
summary: "arXiv preprint"
editPost:
    URL: "https://arxiv.org/abs/2509.13293"
    Text: "arXiv preprint"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2509.13293)


---
##### Abstract
Continuous soil-moisture measurements provide a direct lens on subsurface hydrological processes, notably the post-rainfall "drydown" phase. Because these records consist of distinct, segment-specific behaviours whose forms and scales vary over time, realistic inference demands a model that captures piecewise dynamics while accommodating parameters that are unknown a priori. Building on Bayesian Online Changepoint Detection (BOCPD), we introduce two complementary extensions: a particle-filter variant that substitutes exact marginalisation with sequential Monte Carlo to enable real-time inference when critical parameters cannot be integrated out analytically, and an online-gradient variant that embeds stochastic gradient updates within BOCPD to learn application-relevant parameters on the fly without prohibitive computational cost. After validating both algorithms on synthetic data that replicate the temporal structure of field observations-detailing hyperparameter choices, priors, and cost-saving strategies-we apply them to soil-moisture series from experimental sites in Austria and the United States, quantifying site-specific drydown rates and demonstrating the advantages of our adaptive framework over static models.


---
##### Citation

Gong, M., Nemeth, C., Killick, R., Strauss, P. and Quinton, J. (2025). Inferring Soil Drydown Behaviour with Adaptive Bayesian Online Changepoint Analysis. *arXiv preprint*.

```BibTeX
@article{gong2025inferring,
  title={Inferring Soil Drydown Behaviour with Adaptive Bayesian Online Changepoint Analysis},
  author={Gong, Mengyi and Nemeth, Christopher and Killick, Rebecca and Strauss, Peter and Quinton, John},
  journal={arXiv preprint arXiv:2509.13293},
  year={2025}
}
```