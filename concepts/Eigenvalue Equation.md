---
tags: [linear-algebra]
aliases: [Eigenvalue, Eigenvector, Eigenvectors, Eigenvalues]
date created: Monday, October 17th 2022, 6:56:10 pm
date modified: Thursday, August 20th 2026, 6:23:37 pm
---

# Eigenvalue Equation

## Definition

Let $A \in \mathbb{R}^{n \times n}$ be a [[Square Matrix]], then $\lambda \in \mathbb{R}$ is an [Eigenvalue](Eigenvalue%20Equation.md) of $A$ and $x \in \mathbb{R}^n \setminus \{ 0 \}$ is the corresponding [Eigenvector](Eigenvalue%20Equation.md) of $A$ if the following holds:

$$
Ax = \lambda x
$$

> [!tip] Alternative Form
> The left side of the equation employs [Matrix Multiplication](Matrix%20Multiplication.md) while the right side uses [Matrix Scaling](Matrix%20Scaling.md). An alternative form to use just one type of multiplication is the following.
>
> $$
> Ax = \lambda I x
> $$

## Properties

- The [Rank](Rank.md) of the [[Characteristic Polynomial]] $rk(A - \lambda I_n)$ is less than $n$
- The [Matrix Determinant](Matrix%20Determinant.md) of the [[Characteristic Polynomial]] $det(A - \lambda In)=0$
- The eigenvalue of a matrix is invariant under change of [Basis](Basis.md)

## Eigenvalues as Characteristic Polynomial Roots

The scalar $\lambda \in \mathbb{R}$ is an [Eigenvalue](Eigenvalue%20Equation.md) of $A \in \mathbb{R}^{n \times n}$ if and only if $\lambda$ is a root of the [Characteristic Polynomial](Characteristic%20Polynomial.md) $p_A$ of $A$.

## Uniqueness of Eigenvectors

If $x$ is an [Eigenvector](Eigenvalue%20Equation.md) of $A$ associated with [Eigenvalue](Eigenvalue%20Equation.md) $\lambda$, then for any $c \in \mathbb{R} \setminus \{ 0 \}$ it holds that $cx$ is an eigenvector of $A$ with the same eigenvalue.

$$
A(cx) = cA(x) = c \lambda x=\lambda(cx)
$$

> [!note]
> All vectors that are [Collinear](Collinear.md) to $x$ are also eigenvectors of $A$

## Linear Independence

The [Eigenvectors](Eigenvalue%20Equation.md) $x_1, x_2, \ldots, x_n$ of a [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $A \in \mathbb{R}^{n \times n}$ with $n$ distinct [Eigenvalues](Eigenvalue%20Equation.md) $\lambda_1, \lambda_2, \ldots, \lambda_n$ are [Linearly Independent](Linear%20Independence.md)

> [!NOTE]
> [Eigenvectors](Eigenvalue%20Equation.md) of a [Matrix](Matrix.md) with $n$ distinct [Eigenvalues](Eigenvalue%20Equation.md) form a [Basis](Basis.md) for $\mathbb{R}^n$

## References

1. Mathematics for Machine Learning, Ch.4, pp. 105-107
2. [Eigenvectors & Eigenvalues](https://www.youtube.com/watch?v=PFDu9oVAE-g&t=164s) by 3blue1brown
