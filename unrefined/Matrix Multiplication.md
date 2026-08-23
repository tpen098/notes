---
aliases:
  - Multiplied
  - Matrix Multiplications
  - Matrix Multiply
  - Matrix Product
  - Matrix Products
tags:
  - linear-algebra
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 1:27:58 pm
---

# Matrix Multiplication

## Statement

Let $A = [a_{ij}], B = [b_{ij}] \in M_{m \times n} (\mathbb{R})$. The [[Matrix]] Product AB is $C = [c_{ij}]$ defined as the following

$$ c_{ij} = \sum_{k=1}^p a_{ik} b_{kj}$$

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix}
 , B = \begin{bmatrix}
	b_{11} & b_{12} & \ldots & b_{1n} \\
	b_{21} & b_{22} & \ldots & b_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	b_{m1} & b_{m2} & \ldots & b_{mn}
	\end{bmatrix}
 $$

$$
C
= AB
=
\begin{bmatrix}
		a_{11} & a_{12} & \ldots & a_{1n} \\
		a_{21} & a_{22} & \ldots & a_{2n} \\
		\vdots & \vdots & \ddots & \vdots \\
		a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix}
\begin{bmatrix}
		b_{11} & b_{12} & \ldots & b_{1n} \\
		b_{21} & b_{22} & \ldots & b_{2n} \\
		\vdots & \vdots & \ddots & \vdots \\
		b_{m1} & b_{m2} & \ldots & b_{mn}
\end{bmatrix}
$$

$$
C =
\begin{bmatrix}
	(a_{11}b_{11} + a_{12}b_{21} + \ldots + a_{1n}b_{m1}) &
	(a_{11}b_{12} + a_{12}b_{22} + \ldots + a_{1n}b_{m2}) &
	\ldots &
	(a_{11}b_{1n} + a_{22}b_{2n} + \ldots + a_{2n}b_{mn}) \\

	(a_{21}b_{11} + a_{22}b_{21} + \ldots + a_{2n}b_{m1}) &
	(a_{21}b_{12} + a_{22}b_{22} + \ldots + a_{2n}b_{m2}) &
	\ldots &
	(a_{21}b_{1n} + a_{22}b_{2n} + \ldots + a_{2n}b_{mn}) \\

	\vdots & \vdots & \ddots & \ldots \\

	(a_{m1}b_{11} + a_{m2}b_{21} + \ldots + a_{mn}b_{m1}) &
	(a_{m1}b_{12} + a_{m2}b_{22} + \ldots + a_{mn}b_{m2}) &
	\ldots &
	(a_{m1}b_{1n} + a_{m2}b_{2n} + \ldots + a_{mn}b_{mn}) \\
\end{bmatrix}
$$

> [!warning]
> The column $n$ of $A$ must be equal to row $m$ of $B$.

## Associative Property

$$A(BC) = (AB)C$$

## Noncommutativity

$$AB \neq BA$$

## Identity Property

$$AI_n = I_m A = A$$

## Distributive Property

$$(A + B)C = AC + BC$$

$$C(A + B) = CA + CB$$

## References

1. Elementary Linear Algebra, Ch. 2, pp. 49-53, 63-67
2. Mathematics for Machine Learning, Ch.2, pp. 22-23
