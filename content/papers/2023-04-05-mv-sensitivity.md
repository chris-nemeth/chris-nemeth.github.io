---
title: "Multivariate sensitivity analysis for a large-scale climate impact and adaptation model"
date: 2023-04-05
lastmod: 2023-04-05
tags: ["emulation","Gaussian processes","climate model"]
author: ["Oluwole Oyebamiji","Christopher Nemeth","Paula A Harrison", "Robert W Dunford", "George Cojocaru"]
description: " "
summary: "Journal of the Royal Statistical Society: Series C"
editPost:
    URL: "https://academic.oup.com/jrsssc/article-abstract/72/3/770/7163085?redirectedFrom=fulltext"
    Text: "Journal of the Royal Statistical Society: Series C"

---

---

##### Download

+ [Paper](https://academic.oup.com/jrsssc/article-abstract/72/3/770/7163085?redirectedFrom=fulltext)
+ [arXiv](https://arxiv.org/abs/2201.09681)
+ [Code and data](https://github.com/wolemi2/JRSSC_paper_code)


---
##### Abstract

We develop a new efficient methodology for Bayesian global sensitivity analysis for large-scale multivariate data. The focus is on computationally demanding models with correlated variables. A multivariate Gaussian process is used as a surrogate model to replace the expensive computer model. To improve the computational efficiency and performance of the model, compactly supported correlation functions are used. The goal is to generate sparse matrices, which give crucial advantages when dealing with large datasets, where we use cross-validation to determine the optimal degree of sparsity. This method was combined with a robust adaptive Metropolis algorithm coupled with a parallel implementation to speed up the convergence to the target distribution. The method was applied to a multivariate dataset from the IMPRESSIONS Integrated Assessment Platform (IAP2), an extension of the CLIMSAVE IAP, which has been widely applied in climate change impact, adaptation and vulnerability assessments. Our empirical results on synthetic and IAP2 data show that the proposed methods are efficient and accurate for global sensitivity analysis of complex models.

---
##### Citation

Oyebamiji, O., Nemeth, C., Harrison, P., Dunford, R. and Cojocaru, G., (2023). Multivariate sensitivity analysis for a large-scale climate impact and adaptation model.*Journal of the Royal Statistical Society: Series C.* Vol.72(3), pp. 770–808.

```BibTeX
@article{oyebamiji2023multivariate,
  title={Multivariate sensitivity analysis for a large-scale climate impact and adaptation model},
  author={Oyebamiji, Oluwole Kehinde and Nemeth, Christopher and Harrison, Paula A and Dunford, Robert W and Cojocaru, George},
  journal={Journal of the Royal Statistical Society Series C: Applied Statistics},
  volume={72},
  number={3},
  pages={770--808},
  year={2023},
  publisher={Oxford University Press US}
}
```

