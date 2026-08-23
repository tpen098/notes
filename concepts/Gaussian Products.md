---
aliases: [Gaussian Product]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 9:15:22 pm
date modified: Thursday, August 20th 2026, 6:56:50 pm
---

# Gaussian Products

## Definition

The product of two [[Gaussian Distribution|Gaussians]] $\mathcal{N}(x|a, A) \mathcal{N}(x|b, B)$ is a [[Gaussian Distribution]] $k \mathcal{N}(x|c, C)$ with the following term definitions

$$
\begin{align}
C &= (A^{-1}+B^{-1})^{-1} \\
c &= C(A^{-1}a + B^{-1}b) \\
k &= (2\pi)^{-D/2}|A+B|^{1/2}
\exp\left( -\frac{1}{2} (a-b)^{\top} \\
(A+B)^{-1}(a-b) \right)
\end{align}
$$

## References

1. Mathematics for Machine Learning, p. 201
