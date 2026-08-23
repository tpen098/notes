---
aliases: [Matrix Additions]
tags: [linear-algebra]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 10:25:33 am
---

# Matrix Addition

## Statement

Let $A = [a_{ij}], B = [b_{ij}] \in M_{m \times n} (\mathbb{R})$. The sum of $A$ and $B$ is the [[Matrix]] $C = [c_{ij} = a_{ij} + b_{ij}]$

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
	\vdots & \vdots & \ddots & \vdots \\>
	b_{m1} & b_{m2} & \ldots & b_{mn}
	\end{bmatrix}
 $$

$$
 C = A + B
 	:= \begin{bmatrix}
		a_{11} + b_{11} & a_{12} + b_{12} & \ldots & a_{1n} + b_{1n} \\
		a_{21} + b_{21} & a_{22} + b_{22} & \ldots & a_{2n} + b_{2n} \\
		\vdots & \vdots & \ddots & \vdots \\
		a_{m1} + b_{m1} & a_{m2} + b_{m2} & \ldots & a_{mn} + b_{mn}
	\end{bmatrix}
$$

## Closure Property

$$A + B \in M_{m \times n} (\mathbb{R})$$

## Commutative Property

$$A + B = B + A$$

## Associative Property

$$A + (B + C) = (A + B) + C$$

## Additive Identity

$$A + 0 = 0 + A$$

## Additive Inverse Property

$$ A + (-A) = 0$$

## References

1. Elementary Linear Algebra, Ch. 2, pp. 48-49, 61-63
2. Mathematics for Machine Learning, Ch.2, p. 22
