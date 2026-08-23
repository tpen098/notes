---
tags: [linear-algebra]
aliases: [Inner Products]
date created: Tuesday, September 20th 2022, 1:11:56 pm
date modified: Sunday, August 23rd 2026, 11:53:02 am
---

# Inner Product

## Definition

A [[Symmetric Positive Definite]] [[Bilinear Mapping]] $\Omega: V \times V \rightarrow \mathbb{R}$ is defined as an Inner Product on [[Vector Space]] $V$ [^1]

$$\Omega(x, y) = \langle x, y \rangle$$

Alternatively, it is also defined as the following pair

$$
(V, \langle \cdot, \cdot \rangle)
$$

> [!TLDR] TLDR
> [[Inner Product]] is a measure of similarity

## With Respect to a Basis

Consider a $n$ dimensional [[Vector Space]] $V$ with an [[Inner Product|Inner Product]] $\langle \cdot, \cdot\rangle: V \times V \rightarrow \mathbb{R}$ and an ordered [[Basis]] $B = (b_1,\ldots,b_n)$ of $V$.

Since any vector in $V$ can be written as a [[Linear Combination]] of the basis vectors, the following holds:

$$
\langle x,y\rangle
=
\left\langle
\sum_{i=1}^n\psi_ib_i,\sum_{j=1}^n\lambda_j b_j
\right\rangle
=
\sum_{i=1}^n\sum_{j=1}^n
\psi_i \langle b_i, b_j \rangle \lambda_j
= \hat{x}^{\top} A \hat{y}
$$

## Inner Product Matrix

The [[Symmetric Positive Definite]] $A$ is an [[Inner Product]] with respect to [[Basis]] $B$

$$
A
=
\begin{bmatrix}
	\langle b_1, b_1 \rangle & \ldots & \langle b_1, b_n \rangle \\
	\vdots & \ddots & \vdots \\
	\langle b_n, b_1 \rangle & \ldots & \langle b_n, b_n \rangle
\end{bmatrix}
=
[a_{ij} := \langle b_i, b_j \rangle]
$$

The vectors $\hat{x}, \hat{y}$ are the coordinates of $x, y$ with respect to the basis $B$

$$
\hat{x}
=
\begin{bmatrix}
\psi_1 \\ \ldots \\ \psi_n
\end{bmatrix}

\hat{y}
=
\begin{bmatrix}
\lambda_1 \\ \ldots \\ \lambda_n
\end{bmatrix}
$$

## Example

Consider the [[Vector Space]] $V = \mathbb{R}^2$. The following is an example of an inner product since it is a [[Symmetric Positive Definite]] [[Bilinear Mapping]].

$$
\langle x, y \rangle :=
	x_1 y_1 - (x_1 y_2 + x_2 y_1) + 2 x_2 y_2
$$

> [!tip]
> The [[Dot Product]] is a common example of an inner product.

## Norm Induction

- The [[Inner Product]] induces a [[Norm]] (but not vice versa)
- Not all [[Norm|Norms]] can be written as an [[Inner Product]] (e.g. [[Manhattan Norm]])

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 72-73)
