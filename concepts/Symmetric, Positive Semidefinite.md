---
tags: [linear-algebra]
aliases: [Symmetric Positive Semidefinite Matrix]
date created: Wednesday, October 19th 2022, 2:46:50 pm
date modified: Friday, August 21st 2026, 3:34:13 pm
---

# Symmetric, Positive Semidefinite

## Definition

If the following holds for a [[Symmetric Matrix]] $A$, then it is a [[Symmetric, Positive Semidefinite]] [[Matrix]]

$$
\forall x \in V: x^{\top}Ax \geq 0
$$

where $V$ is a [[Vector Space]].

## Generation Using Self Matrix Transpose

Given a [Matrix](Matrix.md) $A \in \mathbb{R}^{m \times n}$, a [[Symmetric, Positive Semidefinite]] [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $S \in \mathbb{R}^{n \times n}$ can be obtained through self [[Matrix Transpose]].

$$
S := A^{\top}A
$$

## References

1. Mathematics for Machine Learning, Ch.3, pp. 72 - 74
2. Mathematics for Machine Learning, Ch.4, p. 106
