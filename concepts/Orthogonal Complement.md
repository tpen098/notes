---
aliases: [Orthogonal Complements]
tags: [linear-algebra]
date created: Tuesday, September 20th 2022, 9:07:33 pm
date modified: Friday, August 21st 2026, 2:19:35 pm
---

# Orthogonal Complement

## Statement

Consider a $D$-dimensional [[Vector Space]] $V$ and an $M$-dimensional [[Vector Subspace]] $U \subseteq V$.

The [[Orthogonal Complement]] of $U$, denoted as $U^{\top}$ is a $(D-M)$-dimensional subspace of $V$ that contains all vectors in $V$ that are [[Orthogonal]] to every vector in $U$.

## Vector Decomposition

Since $U \cap U^{\top} = \{ 0 \}$, [[Vector Space|Vector]] $x \in V$ can be uniquely decomposed into the following

$$
x
=
\sum_{m=1}^{M} \lambda_m b_m
\sum_{j=1}^{D-M} \psi_j b_j^{\top},
\lambda_m, \psi_j \in \mathbb{R}
$$

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 79-80
