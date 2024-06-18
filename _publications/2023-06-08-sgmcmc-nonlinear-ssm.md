---
title: "Stochastic Gradient MCMC for Nonlinear State Space Models"
collection: publications
permalink: /publication/2023-06-08-sgmcmc-nonlinear-ssm
excerpt: ''
date: 2023-06-08
venue: 'Bayesian Analysis (to appear)'
paperurl: 'https://projecteuclid.org/journals/bayesian-analysis/advance-publication/Stochastic-Gradient-MCMC-for-Nonlinear-State-Space-Models/10.1214/23-BA1395.full'
citation: 'Aicher, C., Putcha, S., Nemeth, C., Fearnhead, P. and Fox, E.B., (2023). &quot;Stochastic Gradient MCMC for Nonlinear State Space Models.&quot; <i>Bayesian Analysis (to appear).</i>'
---
State space models (SSMs) provide a flexible framework for modeling complex time series via a latent stochastic process. Inference for nonlinear, non-Gaussian SSMs is often tackled with particle methods that do not scale well to long time series. The challenge is two-fold: not only do computations scale linearly with time, as in the linear case, but particle filters additionally suffer from increasing particle degeneracy with longer series. Stochastic gradient MCMC methods have been developed to scale inference for hidden Markov models (HMMs) and linear SSMs using buffered stochastic gradient estimates to account for temporal dependencies. We extend these stochastic gradient estimators to nonlinear SSMs using particle methods. We present error bounds that account for both buffering error and particle error in the case of nonlinear SSMs that are log-concave in the latent process. We evaluate our proposed particle buffered stochastic gradient using SGMCMC for inference on both long sequential synthetic and minute-resolution financial returns data, demonstrating the importance of this class of methods.

[arXiv](https://arxiv.org/abs/1901.10568)
[Code](https://github.com/aicherc/sgmcmc_ssm_code)
