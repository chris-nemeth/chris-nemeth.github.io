---
title: "Stochastic gradient MCMC in R"
excerpt: "An R package for stochastic gradient Monte Carlo sampling based on Tensorflow.<br/><img src='/images/sgmcmc-stan-time.jpg'>"
collection: software
---

sgmcmc implements popular stochastic gradient Markov chain Monte Carlo (SGMCMC) methods including stochastic gradient Langevin dynamics (SGLD), stochastic gradient Hamiltonian Monte Carlo (SGHMC) and stochastic gradient Nosé-Hoover thermostat (SGNHT). The package uses automatic differentiation, so all the differentiation needed for the methods is calculated automatically. Control variate methods can be used in order to improve the efficiency of the methods as proposed in the recent publication.

The package is built on top of the TensorFlow library for R, which has a lot of support for statistical distributions and operations, which allows a large class of posteriors to be built. More details can be found at the TensorFlow R library webpage, also see the TensorFlow API for full documentation.

[Github link to package](https://github.com/STOR-i/sgmcmc)
