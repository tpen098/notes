---
aliases: [Solving a Linear System]
tags: [linear-algebra]
date created: Monday, September 12th 2022, 3:27:47 pm
date modified: Friday, August 21st 2026, 3:12:35 pm
---

# Solving Linear Systems

## Gaussian Elimination

Using [[#Gaussian Elimination]], the [[Matrix]] can be converted into [[Matrix Row Echelon Form]]. In this form, the [[Matrix]] can be reverted into a system of [[Linear Equation|Linear Equations]] and more conveniently solved using back substitution

### Example

$$
\left[\begin{array}{rrr|r}
	  1 & 1 & 2 & 8 \\
	  0 & 1 & -5 & -9 \\
	  0 & 0 & 1 & 2 \\
\end{array}\right]
$$

$$
\begin{align}
	 x_3 &= 2 \\
	 x_2 &= -9 + 5 x_3 =1 \\
	 x_1 &= 8 - x_2 - 2x_3 = 3
\end{align}
$$

> [!warning]
> If a row has zero entries but a non-zero $b$, then there is no solution or it is inconsistent

## Gauss-Jordan Reduction

Using [[#Gauss-Jordan Reduction]], the [[Matrix]] can be converted into [[Matrix Row Reduced Row Echelon Form]]. When reverted back into a system of [[Linear Equation|Linear Equations]], the value of each variable is already apparent from the position of the leading entries.

### Example

$$
\left[\begin{array}{rrr|r}
  1 & 0 & 0 & 3 \\
  0 & 1 & 0 & 1 \\
  0 & 0 & 1 & 2 \\
\end{array}\right]
$$

$$
\begin{align}
	 x_3 &= 2 \\
	 x_2 &= 1 \\
	 x_1 &= 3
\end{align}
$$

## Using the Inverse

If $A$ or the coefficient matrix is [[Matrix Inverse|Invertible]], then the system of [[Linear Equation|Linear Equations]] $Ax = b$ has a unique solution $x = A^{-1}b$

### Example

$$(1)
\begin{cases}
	 2x + 3y + z = -1 \\
	 3x + 3y + z = 1 \\
	 2x + 4y + z = -2 \\
\end{cases}

\;\;\;
(2)
\begin{cases}
	 2x + 3y + z = 4 \\
	 3x + 3y + z = 8 \\
	 2x + 4y + z = 5 \\
\end{cases}
$$

$$
A =
\begin{bmatrix}
	2 & 3 & 1 \\ 3 & 3 & 1 \\ 2 & 4 & 1 \\
\end{bmatrix}
\rightarrow
A^{-1} =
\begin{bmatrix}
	-1 & 1 & 0 \\ -1 & 0 & 1 \\ 6 & -2 & -3 \\
\end{bmatrix}
$$

$$
\textbf{x}_1 = A^{-1} \mathbf{b} =
\begin{bmatrix}
	-1 & 1 & 0 \\ -1 & 0 & 1 \\ 6 & -2 & -3 \\
\end{bmatrix}
\begin{bmatrix}
	-1 \\ 1 \\ -2
\end{bmatrix}
=
\begin{bmatrix}
	2 \\ -1 \\ -2
\end{bmatrix}
$$

$$
\textbf{x}_2 = A^{-1} \mathbf{b} =
\begin{bmatrix}
	-1 & 1 & 0 \\ -1 & 0 & 1 \\ 6 & -2 & -3 \\
\end{bmatrix}
\begin{bmatrix}
	4 \\ 8 \\ 5
\end{bmatrix}
=
\begin{bmatrix}
	4 \\ 1 \\ -7
\end{bmatrix}
$$

> [!tip]
> This method is more intensive that prior methods due to needing the [[Matrix Inverse]] but it is best for multiple systems with the same coefficient matrix but different $b$ column vector.

## References

1. Elementary Linear Algebra, Ch. 1, pp. 1-10, 14-15, 19-24
2. Elementary Linear Algebra, Ch. 2, pp. 53-56, 83-84
3. Mathematics for Machine Learning, Ch.2, pp. 22-27
