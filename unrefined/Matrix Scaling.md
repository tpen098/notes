---
aliases:
  - Matrix Scalings
  - Scalar Multiple
  - Scalar Multiples
tags:
  - linear-algebra
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 2:00:11 pm
---

# Matrix Scaling

# Matrix Scaling

## Statement

Let $A = [b_{ij}] \in M_{m \times n} (\mathbb{R}), r \in \mathbb{R}$. The [[Matrix Scaling|Scalar Multiple]] of $A$ and $r$ is the [[Matrix|]] $rA = [r a_{ij}]$

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{12} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix}
$$

$$
rA = \begin{bmatrix}
	ra_{11} & ra_{12} & \ldots & ra_{1n} \\
	ra_{22} & ra_{22} & \ldots & ra_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	ra_{m1} & ra_{m2} & \ldots & ra_{mn}
	\end{bmatrix}
$$

## Closure Property

$$rA \in M_{m \times n} (\mathbb{R})$$

## Associative Property

$$r(sA) = (rs)A$$

$$A(rB) = r(AB) = (rA)B, r \in \mathbb{R}$$

## Distributive Property

$$(r+s) A = rA + sA$$

$$r(A+B) = rA + rB$$

## Multiplicative Identity

$$1 A = A$$

## References

1. Elementary Linear Algebra, Ch. 2, pp. 48-49, 61
2. Mathematics for Machine Learning, Ch.2, pp. 25-26
