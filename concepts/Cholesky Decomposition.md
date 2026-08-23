---
tags: [linear-algebra]
aliases: [Cholesky Factorization, Cholesky Decompositions]
date created: Wednesday, October 19th 2022, 3:12:40 pm
date modified: Sunday, August 16th 2026, 9:39:52 pm
---

# Cholesky Decomposition

## Definition

A [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] $A$ can be factorized into a [[Matrix Multiplication]] of [[Lower Triangular Matrix]] $L$ (that have positive diagonal elements( with the [[Matrix Transpose]] of itself $L^{\top}$.

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
\end{bmatrix}
$$

$$
L = \begin{bmatrix}
	l_{11} & 0 & \ldots & 0 \\
	l_{21} & l_{22} & \ldots & 0 \\
	\vdots & \vdots & \ddots & \vdots \\
	l_{n1} & l_{n2} & \ldots & l_{nn}
\end{bmatrix},
L^{\top} = \begin{bmatrix}
	l_{11} & l_{21} & \ldots & a_{n1} \\
	0 & l_{22} & \ldots & l_{n2} \\
	\vdots & \vdots & \ddots & \vdots \\
	0 & 0 & \ldots & l_{nn}
\end{bmatrix}
$$

$$
A =
\begin{bmatrix}
	l_{11} & 0 & \ldots & 0 \\
	l_{21} & l_{22} & \ldots & 0 \\
	\vdots & \vdots & \ddots & \vdots \\
	l_{n1} & l_{n2} & \ldots & l_{nn}
\end{bmatrix}
\begin{bmatrix}
	l_{11} & l_{21} & \ldots & a_{n1} \\
	0 & l_{22} & \ldots & l_{n2} \\
	\vdots & \vdots & \ddots & \vdots \\
	0 & 0 & \ldots & l_{nn}
\end{bmatrix}
$$

### Cholesky Factor

The [[Matrix]] $L$ is called the Cholesky Factor of $A$ and is unique.

## Three by Three Cholesky Decomposition

$$
\begin{align}
A &=
\begin{bmatrix}
	a_{11} & a_{21} & a_{31} \\
	a_{21} & a_{22} & a_{32} \\
	a_{31} & a_{32} & a_{33} \\
\end{bmatrix}
= LL^{\top}
=
\begin{bmatrix}
	l_{11} & 0 & 0 \\
	l_{21} & l_{22} & 0 \\
	l_{31} & l_{32} & l_{33} \\
\end{bmatrix}
\begin{bmatrix}
	l_{11} & l_{21} & l_{31} \\
	0 & l_{22} & l_{32} \\
	0 & 0 & l_{33} \\
\end{bmatrix}
\\
A &=
\begin{bmatrix}
	l_{11}^2 & l_{21}l_{11} & l_{31}l_{11} \\
	l_{21}l_{11} & l_{21}^2+l_{22}^2 & l_{31}l_{21}+l_{32}l_{22} \\
	l_{31}l_{11} & l_{31}l_{21} + l_{32}l_{22} & l_{31}^2 + l_{32}^2 + l_{33}^2
\end{bmatrix}
\end{align}
$$

### Diagonal Components

$$
\begin{align}
	l_{11} &= \sqrt{a_{11}} \\
	l_{22} &= \sqrt{a_{22} - l_{21}^2} \\
	l_{33} &= \sqrt{a_{33} - (l_{31}^2+l_{32}^2)} \\
\end{align}
$$

### Non-Diagonal Components

$$
\begin{align}
	l_{21} &= \dfrac{1}{l_{11}} a_{21} \\
	l_{31} &= \dfrac{1}{l_{11}} a_{31} \\
	l_{32} &= \dfrac{1}{l_{22}} (a_{32}-l_{31}l_{21})\\
\end{align}
$$

## Determinant of the Cholesky Decomposition

$$
det(A) = det(L)det(L^{\top})=det(L)^2 = \prod_il_{ii}^2
$$

## References

1. Mathematics for Machine Learning, ch.4, p. 114-115
