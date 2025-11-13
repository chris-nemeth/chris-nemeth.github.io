---
title: "Markovian Flow Matching: Accelerating MCMC with Continuous Normalizing Flows" 
date: 2024-10-29
lastmod: 2025-11-12
tags: ["normalizing flows","flow matching", "Markov chain Monte Carlo","sampling"]
author: ["Alberto Cabezas-Gonzalez", "Louis Sharrock", "Christopher Nemeth"]
description: "Blog post on NeurIPS 2024 paper - Markovian Flow Matching: Accelerating MCMC with Continuous Normalizing Flows" 
summary: "Blog post on NeurIPS 2024 paper - Markovian Flow Matching: Accelerating MCMC with Continuous Normalizing Flows" 
cover:
    image: "mfm_figure.png"
    alt: "Gradient Flows"
    relative: false

--- 



In recent years, continuous normalizing flows (CNFs) have gained a lot of traction as a method for generative modelling. In our case, we can use this approach to allow us to establish a continuous, smooth transition between distributions, making CNFs attractive for probabilistic inference tasks where one often needs to sample from complex target distributions. Our recent NeurIPS 2024 paper explores a new approach called Markovian Flow Matching (MFM), which integrates CNFs with Markov Chain Monte Carlo (MCMC) sampling techniques to create an adaptive MCMC algorithm which is well-suited to complex target geometries.

--- 

## Background: The Challenge of Sampling in High Dimensions

Sampling from a probability distribution, particularly in high-dimensional spaces, is a cornerstone problem across fields from Bayesian inference to statistical physics. Let’s define a target probability distribution $\pi(x)$ over a space $\mathbb{R}^d$ that we aim to sample from. Generally, we only know $\pi(x)$ up to a normalizing constant $Z$, i.e., $\pi(x) = \hat{\pi}(x)/Z$, where $\hat{\pi}(x)$ is an unnormalised probability density/mass function.

Traditional MCMC methods, like the Metropolis-Hastings (MH) algorithm, create a Markov chain whose stationary distribution is the target distribution $\pi(x)$. However, MCMC can struggle with slow convergence, especially for multi-modal or high-dimensional distributions.

---

## Our Approach: Markovian Flow Matching

We address these challenges by introducing **Markovian Flow Matching (MFM)**, a method that enhances MCMC by integrating it with **continuous normalizing flows (CNFs)**. CNFs are capable of transforming a simple reference distribution into a complex target distribution through an **ordinary differential equation (ODE)** that describes the transition over time. Here’s a breakdown of how MFM works:

### Flow Matching for CNFs

Our method relies on a **flow matching (FM)** objective, which trains a CNF to match a sequence of intermediate distributions (a “probability path”) from a reference distribution to the target distribution. For instance, given a reference distribution $p_0$ (e.g., a standard Gaussian), we train a CNF to transform samples from $p_0$ to resemble samples from $\pi$.

Mathematically, we define a vector field $v_t$ that determines the ODE governing the CNF:
￼
$$
\frac{\mathrm{d}}{\mathrm{dt}} = v_t(\phi_t(x)), \ \ \ \phi_0(x) = x,
$$
where $\phi: [0,1] \times \mathbb{R}^d \rightarrow \mathbb{R}^d$ is a diffeomorphic map called the *flow*.

Here, $\phi_t$ is the flow that maps $p_0$ to $\pi$ over time $t$. Minimising the flow matching objective,

$$
\mathcal{L}(\theta;\pi) = \mathbb{E}_{t \sim U(0,1), x \sim p_t} [\|v_t^{\theta}(x)-v_t(x)\|^2]
$$


allows us to train a neural network $v_t^\theta(x)$ (parameterised by $\theta$), which approximates the true vector field $v_t(x)$. By minimising the flow matching objective we are able to minimise the discrepancy between the generated and desired probability paths from $p_0$ to $p_1 \approx \pi$ for $t \in [0,1]$, which results in a trained CNF that approximates the target distribution.

### Adaptive MCMC with CNFs

By combining **local MCMC kernels** (such as those used in the Metropolis Adjusted Langevin Algorithm (MALA) or Hamiltonian Monte Carlo (HMC)) with **non-local CNF-based kernels**, Markovian Flow Matching (MFM) creates a robust sampler that can explore challenging distributions effectively. The non-local transitions proposed by the CNF allow the sampler to make larger jumps in distribution space, overcoming bottlenecks associated with local exploration alone.

In addition, we use adaptive tempering to handle multi-modal distributions. This technique gradually increases the “temperature” of the target distribution, starting from an easy-to-sample reference distribution $p_0$ and moving toward the complex target distribution of interest $\pi$. This allows the sampler to overcome local optima, improving convergence to all modes in the target.

## Key Results and Experiments

We tested MFM on a variety of benchmarks:

1.	**Synthetic Multimodal Distributions**: MFM successfully captured all modes in the mixtures of Gaussians experiments, where other methods (like traditional MCMC or variational inference) often failed to explore multiple modes.

2.	**Real-World Applications**: We applied MFM to a log-Gaussian Cox process and a stochastic Allen-Cahn equation model. MFM is highly competitive with other state-of-the-art methods in sample quality and computation time, demonstrating its potential in high-dimensional Bayesian inference.


## Conclusions and Future Work

MFM provides a promising framework for improving MCMC through flow-based transitions, making it adaptable for complex inference tasks in machine learning and statistics. Potential directions include refining the choice of flow architectures and exploring non-asymptotic convergence properties.

For those interested, the full [paper](https://arxiv.org/abs/2405.14392) and code are available on [GitHub](https://github.com/albcab/mfm).


--- 

## References

- Cabezas, A., Sharrock, L. and Nemeth, C. (2024). Markovian Flow Matching: Accelerating MCMC with
Continuous Normalizing Flows. 38th Conference on Neural Information Processing Systems (NeurIPS 2024).