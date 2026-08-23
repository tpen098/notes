---
tags: [linear-algebra]
aliases: [Linearly Independent]
date created: Thursday, September 15th 2022, 9:29:31 pm
date modified: Friday, August 21st 2026, 10:08:08 am
---

# Linear Independence

## Definition of Dependency

Consider a [[Vector Space]] $V$ with $k \in \mathbb{N}$ and $x_1, \ldots, x_k \in V$. If there is a non-trivial [[Linear Combination]] such that $\bf{0} = \sum_{i=1}^k 0 x_i$ is always true with at least one $\lambda_i \neq 0$, the [[Vector Space|Vectors]] are [[Linear Independence|Linearly Independent]]

## Definition of Independence

If only the trivial solution exists $\lambda_1 = \ldots = \lambda_k = 0$, then the vectors are [[Linear Independence|Linearly Independent]]

> [!tip]
> A practical way to check if vectors are linearly independent is to use [[Elementary Transformations#Gaussian Elimination|Gaussian Elimination]]. Write all the vectors as columns of a new matrix. All the vectors are linearly independent if and only if all columns are pivot columns.

## References

1. Mathematics for Machine Learning, Ch.2, pp. 40-44)
