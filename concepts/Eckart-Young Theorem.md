---
aliases: []
tags: [linear-algebra]
date created: Thursday, October 20th 2022, 11:54:24 am
date modified: Thursday, August 20th 2026, 6:21:06 pm
---

# Eckart-Young Theorem

## Definition

Consider a [[Matrix]] $A \in \mathbb{R}^{m \times n}$ of [[Rank]] $r$, and let $B \in \mathbb{R}^{m \times n}$ be a [[Matrix]] of [[Rank]] $k$. For any $k \leq r$ with the definition of [[Low-Rank Matrix Approximation]] in $k$. Then the following holds.

$$
\vec{A(k)} = \min_{rank(B)=k}{\lVert A - B\rVert_2}
$$

$$
{\lVert A - B\rVert_2} = \sigma_{k+1}
$$

This theorem shows that $\vec{A}(k)$ is an optimal, [[Low-Rank Matrix Approximation]] of $A$ using a $k$-rank.

## References

1. Mathematics for Machine Learning, Ch.4, pp. 131-132
