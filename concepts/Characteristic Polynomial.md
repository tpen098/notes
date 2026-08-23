---
aliases: [Characteristic Polynomials]
tags: [linear-algebra]
date created: Monday, October 17th 2022, 6:34:48 pm
date modified: Sunday, August 16th 2026, 9:38:37 pm
---

# Characteristic Polynomial

## Definition

For $\lambda \in \mathbb{R}$ and a [[Square Matrix]] $A \in \mathbb{R}^{m \times n}$, is defined as the the following.

$$
\begin{align}
p_A(\lambda)
&:= det(A - \lambda I)
\\
&:= c_0 + c_1 \lambda + c_2 \lambda^2 + \ldots + c_{n-1}\lambda_{n-1}+(-1)^n\lambda_n
\\
\end{align}
$$

## Coefficient Definition

- $c_0 = det(A)$
- $c_{n-1} = (-1)^{n-1}tr(A)$

## References

1. Mathematics for Machine Learning, Ch. 4, pp. 104-105
