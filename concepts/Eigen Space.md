---
aliases: [Eigen Spaces]
tags: [linear-algebra]
date created: Monday, October 17th 2022, 9:06:35 pm
date modified: Thursday, August 20th 2026, 6:21:28 pm
---

# Eigen Space

## Definition

For a [[Square Matrix]] $A \in \mathbb{R}^{n \times n}$, the set of all [Eigenvectors](Eigenvalue%20Equation.md) of $A$ associated with an [Eigenvalue](Eigenvalue%20Equation.md) $\lambda$ [Spans](Span.md) a [Vector Subspace](Vector%20Subspace.md) of $\mathbb{R}^n$ called the Eigen Space

## Solution Space

If $\lambda$ is an [Eigenvalue](Eigenvalue%20Equation.md) of [[Square Matrix]] $A \in \mathbb{R}^{n \times n}$, then the corresponding eigenspace $E_{\lambda}$ is the solution space of the homogenous system of linear equations $(A - \lambda I)x = 0$.

> [!NOTE]
> Alternatively, the eigenspace $E_{\lambda}$ is the [Kernel](Kernel.md) of $A - \lambda I$

## References

1. Mathematics for Machine Learning, Ch. 4, p. 106
