---
tags: [linear-algebra]
aliases: [Symmetric Positive Definite Matrix]
date created: Tuesday, September 20th 2022, 2:41:12 pm
date modified: Sunday, August 23rd 2026, 11:56:14 am
---

# Symmetric Positive Definite

## Statement

A [[Symmetric Matrix]] $A$ that satisfies the following condition for positive definiteness is a symmetric, positive definite matrix (where $V$ is a [[Vector Space]]).

$$
\forall x \in V \setminus \{0\}: x^{\top}Ax > 0
$$

## Generation Using Self Matrix Transpose

Given a [Matrix](Matrix.md) $A \in \mathbb{R}^{m \times n}$, with [[Rank]] of $n$, then a [[Symmetric Positive Definite]] [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $S \in \mathbb{R}^{n \times n}$ can be obtained through self [[Matrix Transpose]].

$$
S := A^{\top}A
$$

## Example

$$
A
=
\begin{bmatrix}
	a_{u} & a_{w} \\
	a_{w} & a_{v} \\
\end{bmatrix}
=
A^{\top}
$$

$$
\begin{align}
x^{\top}Ax
&=
\begin{bmatrix} x_1 & x_2\end{bmatrix}
\begin{bmatrix}
	a_{u} & a_{w} \\
	a_{w} & a_{v} \\
\end{bmatrix}
\begin{bmatrix} x_1 \\ x_2\end{bmatrix}
\\
&=
a_u x_1^2 + a_w a_w x_1 x_2 + a_v x_2^2
> 0, \forall x \in V \setminus \{ 0 \}
\end{align}
$$

## Kernel of a Symmetric Positive Definite Matrix

The [[Kernel#Kernel|kernel]] of a [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] consists only of the $0$ vector because $x^{\top}Ax \geq 0$ implies $Ax \neq 0$ if $x \neq 0$

## Positive Diagonal Elements

The diagonal elements of a [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] are all positive

## Positive Eigenvalues

A [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] always has positive, real [Eigenvalues](Eigenvalue%20Equation.md)

## References

1. Mathematics for Machine Learning, Ch.3, pp. 72 - 74
2. Mathematics for Machine Learning, Ch.4, p. 106
