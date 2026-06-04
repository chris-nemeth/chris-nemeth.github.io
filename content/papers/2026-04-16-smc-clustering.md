---
title: "Scalable Model-Based Clustering with Sequential Monte Carlo"
date: 2026-04-16
lastmod: 2026-04-16
tags: ["clustering","sequential Monte Carlo","online learning","knowledge base construction"]
author: ["Connie Trojan","Pavel Myshkov","Paul Fearnhead","James Hensman","Tom Minka","Christopher Nemeth"]
description: " "
summary: "The 29th International Conference on Artificial Intelligence and Statistics (AISTATS)"
editPost:
    URL: "https://openreview.net/forum?id=EVDivDL9jD"
    Text: "AISTATS"

---

---


##### Download

+ [Paper](https://openreview.net/pdf?id=EVDivDL9jD)
+ [arXiv](https://arxiv.org/abs/2604.14810)
+ [Code](https://github.com/microsoft/smc-clustering)


---
##### Abstract

In online clustering problems, there is often a large amount of uncertainty over possible cluster assignments that cannot be resolved until more data are observed. This difficulty is compounded when clusters follow complex distributions, as is the case with text data. Sequential Monte Carlo (SMC) methods give a natural way of representing and updating this uncertainty over time, but have prohibitive memory requirements for large-scale problems. We propose a novel SMC algorithm that decomposes clustering problems into approximately independent subproblems, allowing a more compact representation of the algorithm state. Our approach is motivated by the knowledge base construction problem, and we show that our method is able to accurately and efficiently solve clustering problems in this setting and others where traditional SMC struggles.

---
##### Citation

Trojan, C., Myshkov, P., Fearnhead, P., Hensman, J., Minka, T. and Nemeth, C. (2026). Scalable Model-Based Clustering with Sequential Monte Carlo. In *The 29th International Conference on Artificial Intelligence and Statistics*.

```BibTeX
@inproceedings{trojan2026scalable,
  title={Scalable Model-Based Clustering with Sequential Monte Carlo},
  author={Trojan, Connie and Myshkov, Pavel and Fearnhead, Paul and Hensman, James and Minka, Tom and Nemeth, Christopher},
  booktitle={The 29th International Conference on Artificial Intelligence and Statistics},
  year={2026}
}
```
