---
title: "Coin Sampling: How to make Bayesian inference learning-rate free" 
date: 2024-08-22
lastmod: 2024-08-22
tags: ["coin betting","coin sampling","gradient flows","learning-rate-free"]
author: ["Louis Sharrock", "Christopher Nemeth
"]
description: "Blog post on Coin Sampling, a learning-rate-free approach to gradient-based Bayesian inference." 
summary: "Blog post on Coin Sampling, a learning-rate-free approach to gradient-based Bayesian inference." 
cover:
    image: "figure-16-1.png"
    alt: "Coin Sampling"
    relative: false

--- 


Bayesian inference is a cornerstone of modern statistics and machine learning, but its practical implementation often requires meticulous tuning of hyperparameters, particularly the learning rate (also known as the step size). In our ICML 2023 paper, *"Coin Sampling: Gradient-Based Bayesian Inference without Learning Rates,"* we introduce a new approach to gradient-based Bayesian inference that bypasses the need for a learning rate. 

This blog post delves into the details of the coin betting algorithm, a technique from the online learning optimization literature, and how it can be applied in the Bayesian setting where our goal is draw samples from a posterior density (note that this idea is applicable beyond the Bayesian setting for generic sampling problems).

---

## The Sampling Problem in Bayesian Inference

At the heart of Bayesian inference is the need to compute or approximate a posterior distribution $\pi$, which represents our updated beliefs about unknown parameters $x$ after observing data $y$. The posterior density is given by Bayes’ theorem:

$$ \pi(x) := \frac{p(y \mid x) p(x)}{p(y)}, $$

where $p(y \mid x)$ is the likelihood of the data given the unknown parameters, $p(x)$ is the prior distribution, and $p(y)$ is the marginal likelihood. The challenge in Bayesian inference often lies in sampling from this posterior distribution, particularly when $x$ is high-dimensional or when the distribution $\pi$ is complex and does not have a closed-form solution.

## Sampling as an Optimization Problem

Recent work, that was first initiated by [Jordan, Kinderlehrer and Otto (1998)](https://epubs.siam.org/doi/10.1137/S0036141096303359), has shown that sampling from a distribution can be viewed as an optimization problem. Specifically, many sampling methods aim to approximate the target distribution $\pi$ by minimising a divergence between an approximating distribution $\mu$ and the target $\pi$. One common divergence used in this context is the Kullback-Leibler (KL) divergence:

$$ \text{KL}(\mu \| \pi) = \int \mu(x) \log\left(\frac{\mu(x)}{\pi(x)}\right) \mathrm{d}x. $$

The objective is to find the distribution $\mu$ that minimises this divergence, making $\mu$ as close as possible to $\pi$. This can be framed as the following optimization problem:

$$ \mu^* = \arg\min_{\mu \in \mathcal{P}_2(\mathbb{R}^d)} \text{KL}(\mu \| \pi), $$

where $\mathcal{P}_2(\mathbb{R}^d)$ is the space of probability measures with finite second moments.

## Gradient Flows in the Space of Probability Measures

This optimization problem can be solved using gradient-based methods. Just as gradient descent is used to minimise functions in Euclidean space, similar techniques can be applied in the space of probability distributions. In this context, many sampling algorithms can be viewed as implementing a gradient flow in the space of probability measures. The gradient flow describes how an initial distribution $\mu_0$ evolves over time towards the target distribution $\pi$, driven by the steepest descent direction of a chosen divergence, such as the KL divergence (more details to follow in a later section).

In practical terms, Stein Variational Gradient Descent (SVGD)[(Liu and Wang, 2016)](https://arxiv.org/abs/1608.04471) is one such algorithm that uses a gradient flow approach in the space of probability measures to transform a set of particles towards the target distribution. However, these gradient-based methods often require careful tuning of hyperparameters, particularly the learning rate, which determines the step size for each iteration of the algorithm. Selecting an appropriate learning rate is crucial for the convergence and efficiency of the algorithm, but this task can be challenging and time-consuming.

## The Challenge of Tuning Learning Rates


The need to tune learning rates in gradient-based sampling methods is a significant challenge. If the learning rate is too large, the algorithm may overshoot and fail to converge. If it is too small, the algorithm may converge too slowly, requiring a large number of iterations. In high-dimensional settings or complex models, this challenge is exacerbated, making it difficult to find a learning rate that works well across all iterations.

Given the widespread reliance on gradient-based methods in Bayesian inference, and the difficulties associated with learning rate tuning, there is a strong motivation to develop algorithms that can avoid this issue altogether.


## Introducing Coin Betting 

Coin betting, a concept borrowed from convex optimization, offers a novel approach to address the challenge of selecting a learning rate. The core idea is to construct a gradient-based sampling method that inherently avoids the need for learning rate tuning. Before getting into our Coin Sampling algorithm, let’s first start with how coin betting works.

### Coin Betting in Euclidean Optimization

The Coin Betting algorithm was first conceived by [Orabona and Pal](https://arxiv.org/abs/1602.04128) in the field of stochastic optimization and was an important contribution to the growing literature of parameter-free optimization methods. The classic scenario involves a gambler placing bets on a series of coin flips. The wealth of the gambler evolves based on the outcomes of these bets, and the goal is to design a betting strategy that guarantees convergence to an optimal solution.

#### Mathematical Formulation

Consider the optimization problem:

$$ x^* = \arg\min_{x \in \mathcal{X}} f(x), $$

where $f : \mathcal{X} \to \mathbb{R}$ is a convex function. Traditional gradient descent updates the iterate $x_t$ as follows:

$$ x_{t+1} = x_t - \gamma \nabla f(x_t), $$

where $\gamma >0$ is the learning rate. The choice of $\gamma$ is crucial for ensuring convergence.

In the coin betting approach, we can eliminate the need for a predefined learning rate by introducing a betting strategy. Let’s define the wealth $w_t$ of a gambler after $t$ rounds of betting:

$$ w_t = \epsilon + \sum_{i=1}^t c_i x_i, $$

where $\epsilon > 0$ is the initial wealth, $x_i$ is the size of the bet in the $i$-th round, and $c_i$ is the outcome of the $i$-th coin flip, which can be interpreted as the negative subgradient of $f$ at $x_i$, i.e.

$$ c_i = -\nabla f(x_i). $$

The betting strategy is defined such that the bet size $x_i$ is a fraction of the current wealth $w_{i-1}$:

$$ x_i = \beta_i w_{i-1}, $$

where $\beta_i \in [-1, 1]$ is the betting fraction. A common choice for $\beta_i$ is based on the Krichevsky-Trofimov (KT) estimator:

$$\beta_t = \frac{\sum_{i=1}^{t-1} c_i}{t}. $$

The update rule for the gambler’s wealth then becomes:

$$ x_{t+1} = x_0 + \frac{1}{t} \sum_{s=1}^{t} c_s \left( w_0 + \sum_{s=1}^{t-1} \langle c_s, x_s - x_0 \rangle \right), $$

where $\langle \cdot, \cdot \rangle$ denotes the inner product.

#### Illustrative Example

Let's see coin betting in action by considering the optimization of a simple function:

$$f(x)=|x-10|$$

This is same example that is given by Francesco Orabona in his ICML 2020 tutorial on [Parameter-Free Online Optimization](https://parameterfree.com/icml-tutorial/).

 Recall that at each iteration $i$ of the coin betting algorithm, we bet $\pounds x_i$ on the outcome $c_i = -\nabla f(x_i)$, and for the function $f$ we know that the subgradients are $\nabla f(x) \in \{-1,1\}$, i.e. $c_i=\{-1,1\}$.

 So, assuming that we start with initial wealth $w_0=1$, how does the algorithm proceed.

*Iteration 0*
![](./figure-1-1.png)

*Iteration 1*
![](./figure-2-1.png)

*Iteration 2*
![](./figure-3-1.png)

*Iteration 3*
![](./figure-4-1.png)

*Iteration 4*
![](./figure-5-1.png)

*Iteration 5*
![](./figure-6-1.png)

*Iteration 6*
![](./figure-7-1.png)

*Iteration 7*
![](./figure-8-1.png)

*Iteration 8*
![](./figure-9-1.png)

*Iteration 9*
![](./figure-10-1.png)

*Iteration 10*
![](./figure-11-1.png)

*Iteration 11*
![](./figure-12-1.png)

*Iteration 12*
![](./figure-13-1.png)

*Iteration 13*
![](./figure-14-1.png)

*Iteration 14*
![](./figure-15-1.png)

We can see from the steps of the algorithm that we may overshoot the minimum. Therefore, we are often interested in the average of the iterates.
![](./figure-16-1.png)


#### Convergence Analysis

Under suitable conditions, the coin betting algorithm guarantees convergence to the optimal solution $x^* $. Specifically, the expected suboptimality $\mathbb{E}[f(\bar{x}_T)] - f(x^{*})$ after $T$ iterations satisfies:

$$ \mathbb{E}[f(\bar{x}_T)] - f(x^* ) \leq \frac{K \| x^* \| \sqrt{\log(1 + 24T^2 \| x^* \|^2 / \epsilon^2)} + \epsilon}{\sqrt{T}}, $$

where $\bar{x_T} = \frac{1}{T} \sum_{t=1}^T x_t$ is the average iterate, and $K$ is a universal constant.

---


## Coin Sampling for Bayesian Inference: Optimization in the Wasserstein Space

In the realm of Bayesian inference, the goal is to sample from a target distribution $\pi$ rather than finding the minimum of a function (as we've just seen in the optimization setting). So, to create a learning-rate-free Bayesian inference scheme we will need to convert the coin betting optimization algorithm to a sampling algorithm. In our ICML 2023 paper [(Sharrock and Nemeth, 2023)](https://arxiv.org/abs/2301.11294), we extend the coin betting framework from the Euclidean space to the Wasserstein space, which is where probability measures live. 


### Optimization Problem in the Wasserstein Space

The coin sampling algorithm seeks to minimize the KL divergence $\text{KL}(\mu \| \pi)$ between the empirical distribution $\mu_t$ of the particles and the target distribution $\pi$. This minimization can be viewed as solving the following optimization problem in the space of probability distributions:

$$ \mu^* = \arg\min_{\mu \in \mathcal{P}_2(\mathbb{R}^d)} \text{KL}(\mu \| \pi), $$

where $\mathcal{P}_2(\mathbb{R}^d)$ denotes the space of probability measures on $\mathbb{R}^d$ with finite second moments.

Assuming that the objective function $\text{KL}(\mu \| \pi)$ is convex in $\mu$, then the optimization problem is to find the distribution $\mu^* $ that minimises this KL divergence. The solution $\mu^* $ corresponds to the distribution that best approximates the target distribution $\pi$ in the sense of the KL divergence.


### What is a Wasserstein Gradient Flow?

A Wasserstein gradient flow is a mathematical concept used to describe the continuous evolution of a probability distribution $\mu_t$ over time, such that it moves towards the minimiser of a certain functional, like the KL divergence. The *"Wasserstein"* aspect refers to the fact that this evolution is governed by the geometry of the Wasserstein space, a metric space of probability distributions.

In this space, the Wasserstein distance $W_2(\mu, \nu)$ between two distributions $\mu$ and $\nu$ is defined as:

$$ W_2^2(\mu, \nu) = \inf_{\gamma \in \Gamma(\mu, \nu)} \int_{\mathbb{R}^d \times \mathbb{R}^d} \|x - y\|^2 \, \mathrm{d}\gamma(x, y), $$

where $\Gamma(\mu, \nu)$ denotes the set of all couplings (joint distributions) with marginals $\mu$ and $\nu$. The Wasserstein distance captures the *"cost"* of transporting mass from the distribution $\mu$ to $\nu$ and is thus sometimes referred to as the *earth mover's distance.*

A Wasserstein gradient flow can then be understood as the evolution of the distribution $\mu_t$ over time, following the steepest descent direction in the Wasserstein space, to minimise a functional $\mathcal{F}(\mu)$. In our case, this functional is the KL divergence:

$$ \frac{\mathrm{d}\mu_t}{\mathrm{d}t} = -\nabla_{W_2} \text{KL}(\mu_t \| \pi), $$

where $\nabla_{W_2}$ denotes the gradient in the Wasserstein space.

This equation describes the evolution of the distribution $\mu_t$ in such a way that it continuously decreases the KL divergence with respect to the target distribution $\pi$. The distribution $\mu_t$ is thus *"flowing"* toward $\pi$ in the space of distributions, driven by the Wasserstein gradient.



### How Does It Relate to Coin Sampling?

In the coin sampling algorithm, the particles are updated in a way that simulates a discrete-time version of this continuous Wasserstein gradient flow. The particles move according to the gradient of the log-density ratio between the approximating distribution $\mu_t$ and the target distribution $\pi$:

$$ \nabla \log \frac{\mu_t(x)}{\pi(x)}. $$

The coin sampling algorithm incorporates this gradient flow into a betting framework, ensuring that the particles converge towards the target distribution without the need for tuning a learning rate.



### Coin Sampling Algorithm


Here's a step-by-step overview of our coin sampling algorithm, also known as Coin Wasserstein gradient descent:

#### 1. **Initial Setup:**
   - Begin with an initial measure $\mu_0$ and a set of $N$ initial particles $\{x^i_0\}_{i=1}^N$ distributed according to $\mu_0$.
   - Assign an initial wealth $w_0$ to each particle.

#### 2. **Betting Strategy:**
   - For each iteration $t$, compute a bet for each particle based on its current wealth and a betting fraction $\beta_t$.
   - The betting fraction is derived from the accumulated outcomes of past iterations, ensuring that the strategy adapts over time without needing a predefined step size, just in the same way as for coin betting.

#### 3. **Updating Particles:**
   - Update each particle's position by incorporating the computed bets, i.e. 

$$ x^i_{t+1} = x^i_0 + \frac{1}{t} \sum_{s=1}^{t} \nabla \log \frac{\mu_t(x^i_s)}{\pi(x^i_s)} \left( w_0 + \sum_{s=1}^{t-1} \langle \nabla \log \frac{\mu_s(x^i_s)}{\pi(x^i_s)}, x^i_s - x^i_0 \rangle \right), $$

   - The update rule does not require a learning rate, as it is inherently determined by the wealth and betting strategy.



## Practical Implementation

To implement coin sampling, we need to approximate the Wasserstein gradients and one way to do this is via an ensemble of interacting particles. The Stein Variational Gradient Descent (SVGD) algorithm is one such practical algorithm that utilises an ensemble of particles. 

In the paper, we introduced the Coin SVGD algorithm, as a practical learning-rate-free variant of SVGD. The algorithm leverages the coin betting framework to update particles without requiring a predefined learning rate, using kernel methods to approximate gradients in the Wasserstein space.

### The gifs that keep on giffing

Here are a number of simulations on 2-dimensional targets which compared the coin sampling against SVGD, where we do a Goldilocks thing on SVGD and consider some learning rates that are too small, too large and one that is hand-tuned to be just right. 


*Doughnut distribution*
![](donut.gif)

*Neal's funnel distribution*
![](funnel.gif)

*Gaussian distribution*
![](gaussian.gif)

*Mixture of two Gaussians*
![](mixture_two_gaussians.gif)

### Some numerical results from the paper

In the paper we demonstrate the effectiveness of Coin SVGD (and a few other *"coinified"* algorithms) through various numerical experiments, including:

- **Toy Examples:** Demonstrating convergence on some low-dimensional distributions with complex geometries.
- **Bayesian Independent Component Analysis (ICA):** Showing competitive performance compared to SVGD with optimal learning rates, particularly in higher dimensions.
- **Bayesian Logistic Regression:** Achieving robust performance across different learning rate scenarios, outperforming SVGD when suboptimal rates are used.
- **Bayesian Neural Networks and Matrix Factorization:** Illustrating the algorithm's adaptability and efficiency on practical machine learning tasks.

## Conclusion

The coin sampling algorithm (aka Coin Wasserstein gradient descent algorithm) is an interesting (and possibly the first) learning-rate-free gradient-based Bayesian inference scheme. In the paper we show that coin sampling is a robust and scalable solution that eliminates the need for learning rate tuning. In fact, it pretty much always just worked out-of-the-box for the examples that we considered. Hopefully, this work lead others to develop more efficient and user-friendly (i.e. learning rate free) implementations of Bayesian methods for new scientific applications.

For more details on the theoretical underpinnings and empirical performance of coin sampling, you can access the full paper [here](https://arxiv.org/abs/2301.11294). The code is also available on [Github](https://github.com/louissharrock/Coin-SVGD)

---
