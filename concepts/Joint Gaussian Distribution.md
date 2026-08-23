---
aliases: [Joint Gaussian, Joint Gaussian Distributions]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 9:02:49 pm
date modified: Sunday, August 23rd 2026, 11:53:38 am
---

# Joint Gaussian Distribution

## Definition

---

Given two continuous, multivariate [[Random Variable|Random Variables]] $X, Y$ with [[Gaussian Distribution|Gaussian Distributions]] $p(X) \sim \mathcal{N}(\mu_{X}, \Sigma_{X}), p(Y) \sim \mathcal{N}(\mu_{Y}, \Sigma_{Y})$ the [[Joint Gaussian Distribution]] is also a [[Gaussian Distribution]], written in the following notation

$$
p(x, y) = \mathcal{N}
\left(
\begin{bmatrix}
\mu_{x} \\ \mu_{y}
\end{bmatrix}
\begin{bmatrix}
\Sigma_{xx} & \Sigma_{xy} \\
\Sigma_{yx} & \Sigma_{yy}
\end{bmatrix}
\right)
$$

Where the diagonal components $\Sigma_{xx}, \Sigma_{yy}$ are marginal [[Covariance|Covariance Matrices]] for the [[Variance]] of $x$ and $y$ respectively, and $\Sigma_{xy}, \Sigma_{yx}$ are the cross-[[Covariance|Covariance Matrices]] between $x$ and $y$.

## Definition

1. Mathematics for Machine Learning, pp. 198-199
