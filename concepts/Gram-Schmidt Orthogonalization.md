---
aliases: [Gram-Schmidt Orthogonalizations]
tags: [linear-algebra]
date created: Thursday, September 22nd 2022, 6:13:31 pm
date modified: Thursday, August 20th 2026, 7:01:24 pm
---

# Gram-Schmidt Orthogonalization

## Statement

The [[Gram-Schmidt Orthogonalization]] transforms any [[Basis]] $B = (b_1, \ldots, b_n)$ of an $n$-dimensional [[Vector Space]] $V$ into an [[Orthonormal]] basis $U = (u_1, \ldots, u_n)$ that [[Span|spans]] the same [[Vector Space]] $V$.

Each [[Basis]] $u$ is derived iteratively using the [[Projection]] of $b_k$ onto all previously established $u_k$.

$$
\begin{align}
	u_1 &:= b_1 \\
	u_2 &:= b_k - \sum_{[u_1, \ldots, u_{k-1}]} \pi_{u_i}(b_k)
\end{align}
$$

## Dot Product Formulation

Using the [[Dot Product]] as the [[Inner Product]]. The generating formula reduces to the following

$$
u_k
=
b_k - \sum_{i = 1}^{k-1}
\dfrac
{b_k^{\top} u_i}
{u_i^{\top} u_i} u_i
$$

## References

1. Mathematics for Machine Learning, Ch, 3, pp. 89-90
