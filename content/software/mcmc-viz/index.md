---
title: "The MCMC Gallery"
date: 2026-07-30
lastmod: 2026-07-30
tags: ["MCMC", "visualisation", "interactive", "sampling", "teaching"]
author: ["Christopher Nemeth"]
description: "An interactive visual atlas of MCMC algorithms - animated, tunable, and explained in plain language."
summary: "An interactive visualisation tool for exploring MCMC algorithms in the browser."
cover:
    image: "mcmc_gallery.png"
    alt: "The MCMC Gallery"
    relative: false
editPost:
    URL: "https://github.com/chris-nemeth/mcmc-viz"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

# The MCMC Gallery

[**Launch the tool**](https://chris-nemeth.github.io/mcmc-viz/)

The MCMC Gallery is an interactive, browser-based visualisation tool for exploring Markov chain Monte Carlo algorithms. Every method faces the same problem: map out a probability distribution that you can only evaluate point by point. Pick a target distribution — a banana, a ring, a mixture of hills — choose an algorithm, and watch the sampler feel its way across the landscape. You can tune the step size and speed as it runs, and watch the acceptance rate and running mean update live.

The tool is designed for teaching and for building intuition about how different samplers behave — where they mix well, where they struggle, and how their tuning parameters affect performance. It builds on the excellent [mcmc-demo](https://github.com/chi-feng/mcmc-demo) by Chi Feng.

---
## Samplers

The gallery currently includes the following algorithms:

### Standard MCMC methods

- Random Walk Metropolis
- Adaptive Metropolis
- Hamiltonian Monte Carlo
- No-U-Turn Sampler (NUTS)
- Metropolis-adjusted Langevin (MALA)
- Unadjusted Langevin (ULA)
- Stochastic Gradient Langevin Dynamics (SGLD)
- SGLD with Control Variates
- Tuning-free ULA (FUSE)
- Hessian-Hamiltonian Monte Carlo (H2MC)
- Gibbs Sampling
- Differential Evolution MCMC
- Microcanonical HMC

### Non-reversible samplers

- Zig-Zag Sampler
- Bouncy Particle Sampler

### Non-Markovian iterative methods

- Stein Variational Gradient Descent
- Nested Sampling (RadFriends)

---
## Ask a question or open an issue

The source code is available on [GitHub](https://github.com/chris-nemeth/mcmc-viz). Suggestions for new samplers or target distributions are welcome — please open an [issue](https://github.com/chris-nemeth/mcmc-viz/issues) on the repository.
