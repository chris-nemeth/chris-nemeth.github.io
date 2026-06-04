---
title: "Conditioning Gaussian Processes on Almost Anything"
date: 2026-05-20
lastmod: 2026-05-20
tags: ["Gaussian processes","diffusion models","non-conjugate inference","conditioning"]
author: ["Henry Moss","Lachlan Astfalck","Thomas Cowperthwaite","Colin Doumont","Sam Willis","Philipp Hennig","Christopher Nemeth","Andrew Zammit-Mangion"]
description: " "
summary: "arXiv preprint"
editPost:
    URL: "https://arxiv.org/abs/2605.21041"
    Text: "arXiv preprint"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2605.21041)


---
##### Abstract

Gaussian processes (GPs) offer a principled probabilistic model over functions, but exact inference is restricted to the linear-Gaussian regime. We establish an explicit equivalence between GPs and a class of linear diffusion models, recasting predictive sampling as an ODE with closed-form Gaussian dynamics and a likelihood-dependent guidance term that admits a simple Monte Carlo approximation. In the linear-Gaussian setting, we recover standard GP conditioning exactly; beyond conjugacy, the same machinery handles any conditioning statement admitting point-wise likelihood evaluation -- including non-linear physics, and, for the first time, natural language via large language models. Whitening isolates the irreducible non-Gaussian dynamics, minimising Wasserstein-2 transport cost and eliminating numerical stiffness. The result is a general-purpose GP inference scheme requiring no bespoke derivations. Together, these results provide a general mechanism for incorporating the full richness of real-world knowledge as conditioning information, opening a new frontier for the probabilistic modelling of real-world problems.

---
##### Citation

Moss, H., Astfalck, L., Cowperthwaite, T., Doumont, C., Willis, S., Hennig, P., Nemeth, C. and Zammit-Mangion, A. (2026). Conditioning Gaussian Processes on Almost Anything. *arXiv preprint*.

```BibTeX
@article{moss2026conditioning,
  title={Conditioning Gaussian Processes on Almost Anything},
  author={Moss, Henry and Astfalck, Lachlan and Cowperthwaite, Thomas and Doumont, Colin and Willis, Sam and Hennig, Philipp and Nemeth, Christopher and Zammit-Mangion, Andrew},
  journal={arXiv preprint arXiv:2605.21041},
  year={2026}
}
```
