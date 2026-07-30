---
title: "The Sampling Gallery"
date: 2026-07-30
lastmod: 2026-07-30
tags: ["Monte Carlo", "MCMC", "sampling", "visualisation", "interactive", "teaching"]
author: ["Christopher Nemeth"]
description: "An interactive gallery of Monte Carlo, MCMC, and related sampling algorithms - animated, tunable, and explained in plain language."
summary: "An interactive visualisation tool for exploring Monte Carlo, MCMC, and related sampling algorithms in the browser."
cover:
    image: "sampling_gallery.png"
    alt: "The Sampling Gallery"
    relative: false
editPost:
    URL: "https://github.com/chris-nemeth/sampling-viz"
    Text: "GitHub repository"
showToc: true
disableAnchoredHeadings: false

---

# The Sampling Gallery

[**Launch the tool**](https://chris-nemeth.github.io/sampling-viz/)

The Sampling Gallery is an interactive, browser-based collection of Monte Carlo, MCMC, and related sampling algorithms. On paper, each algorithm is only a few lines of mathematics, but its behaviour is not always obvious. These visualisations let you watch a sampler explore a landscape in real time — where it proposes, what it rejects, and how gradients, trajectories, and adaptation shape the search. Pick a target distribution — a banana, a ring, a mixture of hills — choose an algorithm, tune its parameters, and watch it run.

The tool is designed for teaching and for building intuition about how different samplers behave — where they mix well, where they struggle, and how their tuning parameters affect performance. It builds on the excellent [mcmc-demo](https://github.com/chi-feng/mcmc-demo) by Chi Feng.

---
## Samplers

The gallery currently includes the following algorithms:

### Direct and accept-reject methods

- Rejection Sampling

### Weighted Monte Carlo

- Importance Sampling (with optional SIR resampling)

### Markov chain Monte Carlo

- Random Walk Metropolis
- Adaptive Metropolis
- Hamiltonian Monte Carlo
- No-U-Turn Sampler (NUTS)
- Metropolis-adjusted Langevin (MALA)
- Slice Sampling
- Gibbs Sampling
- Hessian-Hamiltonian Monte Carlo (H2MC)
- Unadjusted Langevin (ULA)
- Stochastic Gradient Langevin Dynamics (SGLD), with optional control variates
- Tuning-free ULA (FUSE)

### Ensemble and multimodal methods

- Differential Evolution MCMC
- Parallel Tempering

### Sequential and annealed methods

- Tempered Sequential Monte Carlo (SMC)
- Nested Sampling (RadFriends)

### Non-reversible samplers

- Zig-Zag Sampler
- Bouncy Particle Sampler

### Deterministic and variational particle methods

- Stein Variational Gradient Descent

---
## Ask a question or open an issue

The source code is available on [GitHub](https://github.com/chris-nemeth/sampling-viz). Suggestions for new samplers or target distributions are welcome — please open an [issue](https://github.com/chris-nemeth/sampling-viz/issues) on the repository.
