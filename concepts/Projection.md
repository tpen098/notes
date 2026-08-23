---
aliases: [Projection Matrix, Projections, Projection Matrices]
tags: [linear-algebra]
date created: Thursday, September 22nd 2022, 3:18:55 pm
date modified: Friday, August 21st 2026, 2:36:16 pm
---

# Projection

## Statement

Let $V$ be a [[Vector Space]] and $U \subseteq V$ a [[Vector Subspace]] of $V$.

A [[Linear Mapping]] $\pi: V \rightarrow U$ is called a [[Projection]] if the following holds

$$\pi^2 = \pi \circ \pi = \pi$$

## Matrices Form

Since a [[Linear Mapping]] can be expressed as a [[Transformation Matrix]], the [[Projection]] can be defined using a Projection Matrix $\bf{P_{\pi}}$ with the following property.

$$
P_{\pi}^2
=
P_{\pi}
=
B(B^{\top}B)^{-1} B^{\top}
$$

> [!tip]
> When projecting onto a line, $P_{\pi}=\dfrac{bb^{\top}}{\lVert b \rVert^2}$

### Orthonormal Basis Projection Matrix

If the basis $B$ is an [[Orthonormal Basis]], then the [[Projection]] greatly simplifies to the following

$$
\pi_U(x) = BB^{\top} x
$$

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 81-88
