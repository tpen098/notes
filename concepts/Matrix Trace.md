---
aliases: [Matrix Traces, Trace, Traces]
tags: [linear-algebra]
date created: Monday, October 17th 2022, 6:14:38 pm
date modified: Friday, August 21st 2026, 2:02:30 pm
---

# Matrix Trace

## Definition

The [[Matrix Trace]] of a [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $A$ is defined as the sum of the [[Matrix]]'s diagonal elements.

$$
tr(A) := \sum_{i=1}^{n} a_{ii}
$$

## Definition Using Eigenvalues

The [[Matrix Trace]] of a [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $A \in \mathbb{R}^{n \times n}$ is defined as the sum of its [Eigenvalues](Eigenvalue%20Equation.md) as shown in the following.

$$
tr(A) = \sum_{i=1}^{n}\lambda_i
$$

## Trace of Matrix Sum

$$tr(A+B) = tr(A) + tr(B), A, B \in \mathbb{R}^{m \times n}$$

## Trace of Matrix Scaling

$$tr(\alpha A) = \alpha tr(A), A \in \mathbb{R}^{n \times n}, \alpha \in \mathbb{R}$$

## Trace of Vectors

$$tr(xy^{\top})=tr(y^{\top}x)=y^{\top}x$$

## Invariance in Cyclic Permutations

$$
\begin{align}
tr(A_1 A_2) &= tr(A_2 A_1) \\
tr(A_1 A_2 A_3) &= tr(A_2 A_3 A_1) \\
tr(A_1 A_2\ldots A_n) &= tr(A_2\ldots A_nA_1) \\
\end{align}
$$

## Independence of Basis

Given a [Linear Mapping](Linear%20Mapping.md) $\Phi: V \to V$, where $V$ is a [Vector Space](Vector%20Space.md). Defining the trace of this map using the [[Matrix Trace]] representation of $\Phi$, $\Phi$ can be described using the [Transformation Matrix](Transformation%20Matrix.md).

For a different basis of $V$, the corresponding [[Transformation Matrix]] $B$ of $\Phi$ can be obtained by a basis change of the form $S^{-1}AS$. Using the [[#Invariance of Trace in Cyclic Permutations]], the following holds.

$$
tr(B)=tr(S^{-1}AS)=tr(ASS^{-1})=tr(A)
$$

> [!note] Independent from Basis
> Matrix representations of [[Linear Mapping|Linear Mappings]] are [[Basis]] dependent but the [[Matrix Trace|Trace]] of a [[Linear Mapping]] is independent of the [[Basis]].

## References

1. Mathematics for Machine Learning, Ch.2, pp. 103-104, 113
