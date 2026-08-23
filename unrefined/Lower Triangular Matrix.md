---
tags:
  - linear-algebra
aliases:
  - Lower Triangular Matrices
date created: Wednesday, October 19th 2022, 12:28:20 pm
date modified: Friday, August 21st 2026, 10:20:02 am
---

# Lower Triangular Matrix

## Definition

A [[Lower Triangular Matrix]] is a [[Matrix]] wherein all elements to the right and above the diagonal components are zero.

$$
A = [a_{ij}]:
\begin{cases}
	 a_{ij} = 0 & i < j\\
\end{cases}
$$

$$
A_{m \times n} = \begin{bmatrix}
	a_{11} & 0 & 0 & \ldots & 0 \\
	\vdots & \vdots & \ldots &\ddots & \vdots \\
	a_{(m-2)1} & \ldots & a_{(m-2)(n-2)} & 0 & 0 \\
	a_{(m-1)1} & \ldots & a_{(m-1)(n-2)} & a_{(m-1)(n-1)} & 0 \\
	a_{m1} & \ldots & a_{m(n-2)} & a_{m(n-1)} & a_{mn}
	\end{bmatrix}
$$

## References
