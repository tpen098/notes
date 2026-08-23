---
tags: [linear-algebra]
aliases: [Singular Value Matrices]
date created: Wednesday, October 19th 2022, 7:10:31 pm
date modified: Friday, August 21st 2026, 2:57:00 pm
---

# Singular Value Matrix

## Definition

The [[Singular Value Matrix]] $\Sigma \in \mathbb{R}^{m \times n}$ is similar to a [[Diagonal Matrix]] wherein it only has diagonal components $\sigma_i$ called [[Singular Value Matrix|Singular Value Matrix]] and zero for all other elements. However, a key distinction is that it is not always a [[Square Matrix]] so it must use zero padding.

### $m > n$

$$
\Sigma =
\begin{bmatrix}
	\sigma_1 & \ldots & 0 \\
	0 & \ddots & 0 \\
	0 & \ldots & \sigma_n \\
	0 & \ldots & 0 \\
	\vdots & & \vdots \\
	0 & \ldots & 0 \\
\end{bmatrix}
$$

### $m < n$

$$
\Sigma =
\begin{bmatrix}
	\sigma_1 & \ldots & 0 & 0 & \ldots & 0\\
	0 & \ddots & 0 & \vdots & & \vdots\\
	0 & \ldots & \sigma_m & 0 & \ldots & 0 \\
\end{bmatrix}
$$

> [!note] Equal row and column length
> For $n = m$, the [[Singular Value Matrix]] reverts back into a [[Diagonal Matrix]].

## Uniqueness of the Singular Value Matrix

For a given [[Singular Value Decomposition]], the [[Singular Value Matrix]] is unique.

## References

1. Mathematics for Machine Learning, Ch.4, pp. 119-120
