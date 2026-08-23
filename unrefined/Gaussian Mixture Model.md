---
aliases:
  - Gaussian Mixture Models
tags:
  - statistics-probability
date created: Tuesday, December 6th 2022, 4:06:24 pm
date modified: Friday, August 21st 2026, 3:47:44 pm
---

# Gaussian Mixture Model

## Definition

A [[Gaussian Mixture Model]] is a [[Mixture Model]] of $K$ [[Gaussian Distribution|Gaussians]] $\mathcal{N}(x|\mu_{x}, \Sigma_{x})$ with parameters $\theta := \{ \pi_{k}, \mu_{k}, \Sigma_{k}: k=1, \dots, K \}$

$$
p(x|\theta)
= \sum_{k=1}^{K} \pi_{k} p_{k}(x)
= \sum_{k=1}^{K} \pi_{k} \; \mathcal{N}(x|\mu_{x}, \Sigma_{k})
$$
