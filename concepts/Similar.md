---
tags: [linear-algebra]
aliases: [Similar, Similar Matrices]
date created: Monday, October 17th 2022, 6:10:13 pm
date modified: Sunday, August 23rd 2026, 10:34:33 am
---

# Similar

## Definition

A group of [[Matrix|Matrices]] are considered [[Similar|Similar Matrices]] if they possess the same [Matrix Determinant](Matrix%20Determinant.md).

## Property

For two [[Similar|Similar Matrices]] $A, \tilde{A} \in \mathbb{R}^{n \times n}, \exists S \in \mathbb{R}^{n \times n}$ such that the following holds:

$$
\tilde{A} = S^{-1}AS
$$

$$
det(\tilde{A}) = det(S^{-1}AS) = det(A)det(S^{-1}S)=det(A)
$$

## Eigenvalue Similarity Between Similar Matrices

Similar matrices posses the same [Eigenvalues](Eigenvalue%20Equation.md).

## References

1. Mathematics for Machine Learning, Ch.2, pp. 103, 106
