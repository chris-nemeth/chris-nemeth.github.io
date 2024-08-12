---
title: "Scalable Monte Carlo for Bayesian Learning" 
date: 2024-08-07
lastmod: 2024-08-07
tags: ["Bayesian","Monte Carlo","Scalable"]
author: ["Paul Fearnhead, Christopher Nemeth, Chris J. Oates and Chris Sherlock"]
description: "This book covers recent advances in the Monte Carlo literature for performing Bayesian inference in high-dimensional and large-data settings."
summary: "This book introduces scalable Monte Carlo algorithms for Bayesian inference."
cover:
    image: "img.jpeg"
    alt: "Scalable Monte Carlo for Bayesian Learning"
    relative: false
editPost:
    URL: "https://arxiv.org/abs/2407.12751"
    Text: "Cambridge University Press"
showToc: false
disableAnchoredHeadings: false

---

---

#### Description

This book provides a graduate-level introduction to advanced topics in Markov chain Monte Carlo (MCMC) algorithms, as applied broadly in the Bayesian computational context. Most of these topics, stochastic gradient MCMC, non-reversible MCMC, continuous time MCMC, and new techniques for convergence assessment, have emerged as recently as the last decade. They have driven substantial recent practical and theoretical advances in the field. A particular focus is on methods that are scalable with respect to either the amount of data, or the data dimension, motivated by the emerging high-priority application areas in machine learning and AI.



#### View

+ [Full book](scalable_mcmc_book.pdf)
+ Chapter 1: Background
    - Monte Carlo Methods 
        - What is Monte Carlo Integration? 
        - Importance Sampling 
        - Monte Carlo or Quadrature? 
        - Control Variates 
        - Monte Carlo Integration and Bayesian Statistics 
    - Example Applications 
        - Logistic Regression 
        - Bayesian Matrix Factorisation 
        - Bayesian Neural Networks for Classification 
    - Markov Chains 
        - Reversible Markov chains 
        - Convergence, Averages, and Variances 
    - Stochastic Differential Equations 
        - The Ornstein–Uhlenbeck Process 
        - The Infinitesimal Generator 
        - Langevin Diffusions 
    - The Kernel Trick 
        - Finite-Dimensional Inner Product Spaces 
        - Kernels in a Finite-Dimensional Inner Product Space 
        - A New Inner Product and the Kernel Trick in Finite Dimensions 
        - General Kernels 
        - The Power of the Kernel Trick 
    - Chapter Notes 

+ Chapter 2: Reversible MCMC and its Scaling
    - The Metropolis–Hastings Algorithm 
        - Component-wise updates and Gibbs moves 
        - The Metropolis–Hastings Independence Sampler 
        - The Random Walk Metropolis Algorithm 
        - The Metropolis-Adjusted Langevin Algorithm 
    - Hamiltonian Monte Carlo 
    - Chapter Notes 

+ Chapter 3: Stochastic Gradient MCMC Algorithms
    - The Unadjusted Langevin Algorithm 
    - Approximate vs. Exact MCMC 
    - Stochastic Gradient Langevin Dynamics 
        - Controlling Stochasticity in the Gradient Estimator 
        - Example: The Value of Control Variates 
        - Convergence Results for Stochastic Gradient Langevin Dynamics 
    - A General Framework for stochastic gradient MCMC 
    - Guidance for Efficient Scalable Bayesian Learning 
        - Experiments on a Logistic Regression Model 
        - Experiments on a Bayesian Neural Network Model 
    - Generalisations and Extensions 
        - Scalable Inference for Models in Constrained Spaces 
        - Scalable Inference with Time Series Data 
    - Chapter Notes

+ Chapter 4: Non-Reversible MCMC
    - The Benefits of Non-Reversibility 
    - Hamiltonian Monte Carlo Revisited 
    - Lifting Schemes for MCMC 
        - Non-Reversible HMC 
        - Gustafson’s Algorithm and Multidimensional Generalisations 
    - Improving Non-reversibility: Delayed Rejection 
        - The Discrete Bouncy Particle Sampler 
    - Chapter Notes


+ Chapter 5: Continuous-Time MCMC
    - Continuous-Time MCMC as the Limit of Non-Reversible MCMC 
    - Piecewise Deterministic Markov Processes 
        - What is a PDMP? 
        - Simulating PDMPs 
        - The Generator and Invariant Distribution of a PDMP 
        - The Limiting Process of Section 5.1 as a PDMP 
    - Continuous-time MCMC via PDMPs 
        - Different Samplers 
        - Use of PDMP Output 
        - Comparison of Samplers 
    - Efficient Simulation of PDMP Samplers 
        - Simulating PDMPs 
        - Exploiting Model Sparsity
        - Data Subsampling Ideas 
    - Extensions 
        - Discontinuous Target Distribution 
        - Reversible Jump PDMP Samplers 
        - More General Velocity Models 
    - Chapter Notes


+ Chapter 6: Assessing and Improving MCMC
    - Diagnostics for MCMC 
        - Convergence Diagnostics 
        - Bias Diagnostics 
        - Improved Bias Diagnostics via the Kernel Trick 
    - Convergence Bounds for MCMC 
        - Bounds on Integral Probability Metrics 
        - Choice of Auxiliary Markov Process 
        - Kernel Stein Discrepancy 
        - Convergence Control 
        - Stochastic Gradient Stein Discrepancy 
    - Optimal Weights for MCMC 
    - Optimal Thinning for MCMC 
    - Chapter Notes 
---

#### Citation

Fearnhead, P., Nemeth, C., Oates, C.J. and Sherlock, C., 2024. Scalable Monte Carlo for Bayesian Learning. arXiv preprint arXiv:2407.12751.

```BibTeX
@book{fearnhead2024scalable,
  title={Scalable Monte Carlo for Bayesian Learning},
  author={Fearnhead, Paul and Nemeth, Christopher and Oates, Chris J and Sherlock, Chris},
  publisher={Cambridge University Press},
  year={2024}
}
```