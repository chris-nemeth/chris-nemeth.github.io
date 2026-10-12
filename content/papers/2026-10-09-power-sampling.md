---
title: "A Critical Look at Power Sampling when Test Time Sharpening LLMs"
date: 2026-10-09
lastmod: 2026-10-09
tags: ["large language models","power sampling","test-time sharpening","sequential Monte Carlo"]
author: ["Abiel Malkani Talwar","Christopher Nemeth","Henry Moss"]
description: " "
summary: "arXiv preprint"
editPost:
    URL: "https://arxiv.org/abs/2610.13653"
    Text: "arXiv preprint"

---

---


##### Download

+ [arXiv](https://arxiv.org/abs/2610.13653)


---
##### Abstract

Reinforcement learning with verifiable rewards (RLVR) has substantially improved LLM reasoning, yet growing evidence suggests it mainly performs distribution sharpening: concentrating probability mass on reasoning paths the base model already produces. Recent work therefore seeks RLVR's gains without needing reward signals, by sampling from the power distribution $\pi_\alpha \propto \pi_{\text{base}}^\alpha$ via Markov chain Monte Carlo or sequential Monte Carlo. We show that these samplers fail to converge to $\pi_\alpha$ under realistic compute budgets, and that their gains are largely recreated via simple Best-of-$N$ with appropriate grading. This suggests they succeed by selecting high-probability sequences, not by approximating $\pi_\alpha$, raising a natural question: is the power distribution itself a worthwhile target? We test this hypothesis directly by fine-tuning the base model to match $\pi_\alpha$, sidestepping sampler convergence issues entirely. Despite approximating the target far more faithfully than existing samplers, this strategy yields gains that are noisy and specific to certain models and sampling tasks. Together, our results suggest that the value of power sampling lies not in faithfully targeting $\pi_\alpha$, but in the simpler goal of extracting sequences the base model already deems likely.

---
##### Citation

Malkani Talwar, A., Nemeth, C. and Moss, H. (2026). A Critical Look at Power Sampling when Test Time Sharpening LLMs. *arXiv preprint*.

```BibTeX
@article{malkanitalwar2026critical,
  title={A Critical Look at Power Sampling when Test Time Sharpening LLMs},
  author={Malkani Talwar, Abiel and Nemeth, Christopher and Moss, Henry},
  journal={arXiv preprint arXiv:2610.13653},
  year={2026}
}
```
