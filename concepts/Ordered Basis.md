---
aliases: [Ordered Bases]
tags: [linear-algebra]
date created: Wednesday, October 19th 2022, 2:18:48 pm
date modified: Friday, August 21st 2026, 2:17:56 pm
---

# Ordered Basis

Definition

Consider a [[Basis]] $\{ b_1, \ldots, b_n \}$ of an $n$-dimensional [[Vector Space]] $V$. If the order of the [[Basis]] is important then it can be written as an $n$-tuple called the [[Ordered Basis|Ordered Bases]] of $V$

$$
B = ( b_1, \ldots, b_n )
$$

## Coordinate Representation

Consider a [[Vector Space]] $V$ and an [[Ordered Basis]] $B = (b_1, \ldots, b_n)$ of $V$. For any $x \in V$ there is a unique representation or [[Linear Combination]].

$$
x = \alpha_1 b_1 + \ldots + \alpha_n b_n
$$

Then $\alpha_1, \ldots, \alpha_n$ are the coordinates of $x$ with respect to $B$.

This can be written as a coordinate vector or coordinate representation of $x$ with respect to ordered basis $B$

$$
\alpha
=
\begin{bmatrix}
	\alpha_1 \\
	\vdots \\
	\alpha_n \\
\end{bmatrix}
\in \mathbb{R}^n
$$

> [!NOTE] Coordinate System
> A basis effectively defines a coordinate system

## References

1. Mathematics for Machine Learning, Ch.2, pp. 44-47, 50-51
