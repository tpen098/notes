---
tags: [linear-algebra]
aliases: [Diagonal Matrices]
date created: Wednesday, October 19th 2022, 3:49:05 pm
date modified: Tuesday, August 18th 2026, 9:47:10 pm
---

# Diagonal Matrix

## Definition

A [[Diagonal Matrix]] is a [[Square Matrix]] wherein all non-diagonal elements in the [[Matrix]] are zero-valued.

$$D_n =
\begin{bmatrix}
	d_1 & 0 & 0 & \ldots & 0 \\
	0 & d_2 & 0 &\ldots & 0 \\
	0 & 0 & d_3 & \ldots & 0 \\
	\vdots & \vdots & \vdots &\ddots & \vdots \\
	0 & 0 & 0 &\ldots & d_n
\end{bmatrix}
$$

## Determinant of a Diagonal Matrix

$$
det(D_n) = \prod_{i=1}^{n} d_{i}
$$

## Inverse of a Diagonal Matrix

$$
D_n^{-1} =
\begin{bmatrix}
	d_1^{-1} & 0 & 0 & \ldots & 0 \\
	0 & d_2^{-1} & 0 &\ldots & 0 \\
	0 & 0 & d_3^{-1} & \ldots & 0 \\
	\vdots & \vdots & \vdots &\ddots & \vdots \\
	0 & 0 & 0 &\ldots & d_n^{-1}
\end{bmatrix}
$$

> [!warning] Division by Zero
> This holds assuming all diagonal components are nonzero.

## Powers of a Diagonal Matrix

$$
D_n^k =
\begin{bmatrix}
	d_1^k & 0 & 0 & \ldots & 0 \\
	0 & d_2^k & 0 &\ldots & 0 \\
	0 & 0 & d_3^k & \ldots & 0 \\
	\vdots & \vdots & \vdots &\ddots & \vdots \\
	0 & 0 & 0 &\ldots & d_n^k
\end{bmatrix}
$$

## References

1. Mathematics for Machine Learning, Ch.4, pp. 115-116
