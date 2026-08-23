---
aliases:
  - Probabilistic PCA
tags:
  - statistics-probability
date created: Wednesday, November 30th 2022, 6:06:23 pm
date modified: Friday, August 21st 2026, 2:29:53 pm
---

# Probabilistic Principal Component Analysis

Given a [[Model Input]] [[Independent and Identically Distributed|IID Dataset]] $\mathcal{X} = \{ x_{1}, \dots, x_{N} \}, x_{n} \in \mathbb{R}^{D}$ with [[Transfer Function Roots|Zero]] [[Mean]] $\mu = 0$ and a [[Covariance|Covariance Matrix]] $S$ as shown

$$
S
= \frac{1}{N} \sum_{n=1}^N x_{n} x^{\top},
= \frac{1}{N} X X^{\top}
, X \in \mathbb{R}^{D \times N}
$$

There exists a [[Low-Dimensional Encoding|Low-Dimensional Representation]]
