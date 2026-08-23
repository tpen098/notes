---
aliases:
  - Bilinear
  - Bilinear Mappings
tags:
  - mathematics
date created: Tuesday, September 20th 2022, 1:14:00 pm
date modified: Tuesday, August 18th 2026, 9:22:16 pm
---

# Bilinear Mapping

## Statement

Let $V$ be a [[Vector Space]] and $\Omega: V \times V \rightarrow \mathbb{R}$ be a [[Bilinear Mapping]] that takes two [[Vector Space|Vectors]] and maps them to a linear number.

## Properties

Consider a [[Vector Space]] $V$, for all $x, y, z \in V, \lambda, \psi \in \mathbb{R}$, the following holds for a [[Bilinear Mapping]]:

$$
\begin{align}
	\Omega (\lambda x + \psi y, z)
	&= \lambda \Omega(x, z) + \psi \Omega(y, z)
	\\
	\Omega (x, \lambda y + \psi z)
	&= \lambda \Omega(x, y) + \psi \Omega(x, z)
\end{align}
$$

## Symmetric

A [[Bilinear Mapping]] is symmetric if the order of the arguments do not matter

$$
\Omega(x, y) = \Omega(y, x), \forall x, y \in V
$$

## Positive Definite

A [[Bilinear Mapping]] is positive definite if the following holds:

$$
\forall x \in V \setminus \{ 0\}:
\Omega(x, x) > 0, \Omega(0, 0) = 0
$$

## References

1. Mathematics for Machine Learning, ch.3, p. 72-73
