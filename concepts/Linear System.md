---
tags: [linear-algebra]
aliases: [Linear Systems, Augmented Matrix]
date created: Thursday, September 15th 2022, 6:18:58 pm
date modified: Friday, August 21st 2026, 10:10:11 am
---

# Linear System

## Definition

A system of $m$ [[Linear Equation|Linear Equations]] in $n$ variables is defines as the following:

$$
\begin{cases}
	a_{11} x_1 + a_{12} x_2 + \ldots + a_{1n} x_n = b_1 \\
	a_{21} x_1 + a_{22} x_2 + \ldots + a_{2n} x_n = b_2 \\
	\ldots \\
	a_{m1} x_1 + a_{m2} x_2 + \ldots + a_{mn} x_n = b_m \\
\end{cases}
$$

## Consistent System

- The system has exactly one solution
- The system has an infinite number of solutions

## Inconsistent System

- The system has no solution

## Compact Matrix Representation

$$
\begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
\end{bmatrix}
\begin{bmatrix}
	x_1 \\ x_2 \\ \vdots \\ x_m
\end{bmatrix}
=
\begin{bmatrix}
	b_1 \\ b_2 \\ \vdots \\ b_m
\end{bmatrix}
$$

> [!note]
> The matrix containing the coefficients of the system (left) is called the **coefficient matrix**

## Augmented Matrix Form

For convenience, the [[Matrix|matrix]] can be written in the following form where the constant terms are listed alongside the coefficient matrix

$$
\left[\begin{array}{rrrr|r}
	a_{11} & a_{12} & \ldots & a_{1n} & b_1\\
	a_{21} & a_{22} & \ldots & a_{2n} & b_2\\
	\vdots & \vdots & \ddots & \vdots & \vdots\\
	a_{m1} & a_{m2} & \ldots & a_{mn} & b_m\\
  \end{array}\right]
$$

## References

1. Elementary Linear Algebra, Ch. 1, pp. 1-10, 14-15, 19-24
2. Elementary Linear Algebra, Ch. 2, pp. 53-56, 83-84
3. Mathematics for Machine Learning, Ch.2, pp. 22-27
