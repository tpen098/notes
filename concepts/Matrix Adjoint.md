---
aliases: [Matrix Adjoints, Adjoint, Adjoints]
tags: [linear-algebra]
date created: Tuesday, September 13th 2022, 10:49:59 pm
date modified: Friday, August 21st 2026, 10:26:08 am
---

# Matrix Adjoint

## Statement

The [[Matrix Adjoint|Adjoint]] of a [[Square Matrix]] $A_n$ is the [[Matrix Transpose]] of the cofactor matrix $C = [c_{ij} = A_{ij}]$ (as defined in [[Matrix Determinant]])

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix}
$$

$$
C = \begin{bmatrix}
	+M_{11} & -M_{12} & +M_{13} &\ldots & -M_{1n} \\
	-M_{21} & +M_{22} & -M_{12} & \ldots & +M_{2n} \\
	+M_{21} & -M_{22} & +M_{12} & \ldots & -M_{2n} \\
	\vdots & \vdots & \vdots & \ddots & \vdots \\
	-M_{n1} & +M_{n2} & -M_{n3} & \ldots & +M_{nn}
	\end{bmatrix}
$$

$$
adj(A) = C^{\top} =
	\begin{bmatrix}
		+M_{11} & -M_{21} & +M_{31} &\ldots & -M_{n1} \\
		-M_{12} & +M_{22} & -M_{32} & \ldots & +M_{n2} \\
		+M_{13} & -M_{23} & +M_{33} & \ldots & -M_{n2} \\
		\vdots & \vdots & \vdots & \ddots & \vdots \\
		-M_{1n} & +M_{2n} & -M_{3n} & \ldots & +M_{nn}
	\end{bmatrix}
$$

## References

1. Elementary Linear Algebra. Ch.3, pp. 158-160
