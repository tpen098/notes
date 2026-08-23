---
aliases: [Variances]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 3:03:05 pm
date modified: Friday, August 21st 2026, 3:42:47 pm
---

# Variance

## Univariate Definition

The [[Covariance]] of a univariate [[Random Variable]] $X$ with itself $Cov[x, x]$ is referred to as the [[Variance]] $\mathbb{V}_{X}[x]$.

$$
\mathbb{V}_{X}[x]
= Cov_{X, X}[x, x]
= \mathbb{E}_{X, X}[x^2] - \mathbb{E}_{X}[x]^2
$$

Alternatively, if the [[Mean]] of the [[Random Variable]] $\mu$ is known, then the [[Covariance]] can be defined as the following

$$
\mathbb{V}_{X}[x] := \mathbb{E}_{X}[(x-\mu)^2]
$$

## Covariance Matrix

 Alternatively, the [[Variance]] between a multivariate [[Random Variable|Random Variables]] $X \in \mathbb{R}^D$ with itself can be defined using a [[Covariance|Covariance Matrix]] as shown in the following

$$
\mathbb{V}_{X}[x] = Cov_{X, X}[x, x] =
\begin{bmatrix}
Cov[x_{1}, x_{1}] & \dots & Cov[x_{1}, y_{D}] \\
\vdots & \ddots & \vdots \\
Cov[x_{D}, x_{1}] & \dots & Cov[x_{D}, x_{D}]
\end{bmatrix}
$$

## Variance of Random Variable Sums

The [[Variance]] of the sum of two [[Random Variable]] $X, Y$ can be redefined as the following

$$
\mathbb{V}[x+y]
= \mathbb{V}[x]
+ \mathbb{V}[y]
+ Cov[x, y]
+ Cov[y, x]
$$

## Variance of Random Variable Differences

The [[Variance]] of the difference of two [[Random Variable]] $X, Y$ can be redefined as the following

$$
\mathbb{V}[x-y]
= \mathbb{V}[x]
+ \mathbb{V}[y]
- Cov[x, y]
- Cov[y, x]
$$

## Variance of an Affine Transformation

Given a [[Random Variable]] $X$ with an [[Affine Transformation]] $y = Ax + b$, the [[Variance]] is defined as the following

$$
\mathbb{V}_{Y}[y]
= V_{X}[Ax+b]
= V_{X}[Ax]
= A V_{X}[x] A^{-\top}
$$

> [!NOTE] Bias
> The Bias of the Affine Transformation doesn't affect the final [[Variance]]

## References

1. Mathematics for Machine Learning, pp. 190,193-194
