---
aliases: [Matrix Transpose, Matrix Transposes, Transpose, Transposes, Matrix Transposition, Matrix Transpositions, Transposition, Transpositions]
tags: [linear-algebra]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 2:03:36 pm
---

# Matrix Transpose

## Statement

Let $A = [a_{ij}] \in M_{m \times n} (\mathbb{R})$. The [[Matrix Transpose]] of $A$ is the $n \times m$ [[Matrix|matrix]] $A^{\top}=[a{ij}^{\top} = a_{ji}]$

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix}
 $$

$$
A^{\top} = \begin{bmatrix}
	a_{11} & a_{21} & \ldots & a_{m1} \\
	a_{12} & a_{22} & \ldots & a_{m2} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{1n} & a_{2n} & \ldots & a_{mn}
	\end{bmatrix}
$$

## Transpose Applied Twice

$$(A^{\top})^{\top} = A$$

## Transpose of Matrix Addition

$$(A + B)^{\top} = A^{\top} + B^{\top}$$

## Transpose of Matrix Scaling

$$(rA)^{\top} = rA^{\top}, r \in \mathbb{R}$$

## Transpose of Matrix Multiplication

$$(AB)^{\top} = B^{\top}A^{\top}$$

## Eigenvalue Consistency

A [[Matrix]] and its [[Matrix Transpose|Transpose]] have the same [Eigenvalues](Eigenvalue%20Equation.md), but not necessarily the same [Eigenvectors](Eigenvalue%20Equation.md)

## References

1. Elementary Linear Algebra, Ch. 2, pp. 67-70)
2. Mathematics for Machine Learning, Ch.2, p. 25
3. Mathematics for Machine Learning, Ch.3, p. 106
