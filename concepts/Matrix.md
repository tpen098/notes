---
tags: [linear-algebra]
aliases: [Matrices]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 10:24:56 am
---

# Matrix

## Definition

An $m \times n$ [[Matrix]] $A$ over $\mathbb{X}$ is a rectangular array of $\mathbb{x} \in \mathbb{X}$ numbers arranged in $m$ rows (horizontal) and $n$ columns (vertical). Each entry or element in the matrix is denoted by its row and column indices $(i, j)$.

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
	\end{bmatrix} = [a_{ij}] \in \mathbb{R}^{m \times n}
$$

> [!note] Equality
> Two [[Matrix|Matrices]] are equal if $a_{ij} = b_{ij}$ for all cases

## Terminologies

### Diagonals

Entries with the equal row and column indices ($a_{11}, a_{22}, \ldots$)

### Pivot

The leading entry of a column or row is called the pivot

## References

1. Elementary Linear Algebra, Ch. 1, pp. 14-15
2. Elementary Linear Algebra, Ch. 2, pp. 46-47
