---
aliases: [Eigendecompositions]
tags: [linear-algebra]
date created: Wednesday, October 19th 2022, 4:09:35 pm
date modified: Thursday, August 20th 2026, 6:22:34 pm
---

# Eigendecomposition

## Statement

A [[Square Matrix]] $A$ can be factored into the following

$$
A = PDP^{-1}
$$

Where $P = [p_1 \ldots p_n]$ are [[Linear Independence|Linearly Independent]] [[Eigenvalue Equation|Eigenvectors]] of $A$ that should form a [[Basis]] for $\mathbb{R}^n$, and $D$ is a [[Diagonal Matrix]] whose diagonal entries are the [[Eigenvalue Equation|Eigenvalues]] of $A$.

> [!Note] Orthogonality of $P$
> The [[Square Matrix]] $P$ is an [[Orthogonal Matrix]]

## Geometrical Intuition

- $P^{-1}$ performs a [[Basis Change]] from the current [[Basis]] to the _Eigen basis_
- $D$ scales the vectors in the Eigen basis
- $P$ undoes the [[Basis Change]] done by $P^{-1}$

![[Eigendecomposition.png|700]]

## Derivation

$$
\begin{align}
A = PDP^{-1} &\to AP = PD\\
AP
&= A [p_1, \ldots, p_n]
= [Ap_1, \ldots, Ap_n]
\\
PD
&= [p_1, \ldots, p_n]
\begin{bmatrix}
	d_1 & \ldots & 0 \\
	\vdots & \ddots & \vdots\\
	0 & \ldots & d_n
\end{bmatrix}
= [\lambda_1 p_1, \ldots, \lambda_n p_n]
\end{align}
$$

The prior equations imply the following relation

$$
\begin{matrix}
	& A p_1 = \lambda_1 p_1 & \\
	& \vdots & \\
	& A p_n = \lambda_n p_n & \\
\end{matrix}
$$

## Determinant of the Eigendecomposition

$$
\begin{align}
det(A)
   &= det(PDP^{-1}) \\
   &= det(P)det(D)det(P^{-1}) \\
   &= det(D) \\
   &= \prod_i^nd_i = \prod_i^n \lambda_i
\end{align}
$$

## Power of the Eigendecomposition

$$
A^k = (PDP^{-1})^k = PD^kP^{-1}
$$

> [!note] Inverse Powers
> This also works for finding the Inverse of the Eigendecomposition

## References

1. Mathematics for Machine Learning, Ch.4, pp. 116-119
