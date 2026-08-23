---
tags: [linear-algebra]
aliases: [SVD, Reduced SVD, Reduced Singular Value Decomposition, Singular Value Decompositions, Reduced Singular Value Decompositions]
date created: Wednesday, October 19th 2022, 7:04:18 pm
date modified: Friday, August 21st 2026, 2:54:56 pm
---

# Singular Value Decomposition

## Statement

Let $A \in \mathbb{R}^{m \times n}$ be a [[Matrix]] of [[Rank]] $r \in [0, min(m, n)]$. The [[Singular Value Decomposition]] is a decomposition with an [[Orthogonal Matrix]] $U \in \mathbb{R}^{m \times m}$, [[Orthogonal Matrix]] $V \in \mathbb{R}^{n \times n}$ and [[Singular Value Matrix]] $\Sigma \in \mathbb{R}^{m \times n}$,

$$
A = U \Sigma V^{\top}
$$

- Columns $u_i$ of the $U$ matrix are called _Left-Singular Vectors_
- Columns $v_j$ of the $V$ matrix are called _Right-Singular Vectors_

## Geometrical Intuition

- $V^{\top}$ performs a [[Basis Change]] from the current basis to the canonical basis of $\mathbb{R}^n$
- $\Sigma$ scales the basis vectors and maps from $\mathbb{R}^n$ to $\mathbb{R}^m$
- $U$ performs another [[Basis Change]] from the current basis to the canonical basis of $\mathbb{R}^m$


![[Singular Value Decomposition.png|700]]

## Reduced Form

A variant to the [[Singular Value Decomposition]] is the [[Singular Value Decomposition|Reduced Singular Value Decomposition]] wherein the [[Singular Value Matrix]] is kept as a [[Square Matrix]] $\Sigma \in \mathbb{R}^{n \times n}$ but $U \in \mathbb{R}^{m \times n}$ is now not a Square Matrix.

- This alters [[Solving for Singular Value Decomposition]] but the mathematical structure is the same for the normal form
- This makes the [[Singular Value Matrix]] a [[Diagonal Matrix]] for convenience.

## References

1. Mathematics for Machine Learning, Ch.4, pp. 119-129
