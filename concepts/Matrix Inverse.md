---
aliases: [Matrix Inverses, Regular, Nonsingular, Inverse, Invertible]
tags: [linear-algebra]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 1:26:57 pm
---

# Matrix Inverse

## Row Reduced Echelon Form Method

The [[Matrix Inverse]] of a [[Square Matrix]] can be obtained by treating its [[Identity Matrix]] as the solution in an [[Solving Linear Systems#Augmented Matrix|augmented matrix]], and then converting the left side into [[Matrix Row Reduced Row Echelon Form]].

$$
\begin{align}
	I_n &= \left(\prod E_i\right)A \\
	A^{-1} &= \left(\prod E_i\right)
\end{align}
$$

$$
\begin{align}
	\left(\prod E_i\right) [A | I_n]
		&= \left[\left(\prod E_i\right) A | \left(\prod E_i\right) I_n \right] \\
	\left(\prod E_i\right) [A | I_n]
		&= [I_n | A^{-1}]
\end{align}
$$

> [!note]
> Of the inverse of a matrix does not exist, the matrix is called **regular** or **nonsingular**

> [!warning]
> If the left side matrix cannot be converted into the identity matrix using row operations, then it isn't singular (or it's not invertible)

## Example

$$
\begin{align}
	A = \begin{bmatrix}
		2 & 0 & 6 \\ -1 & 5 & 3 \\ 1 & 3 & -1
	\end{bmatrix}
	\rightarrow

	\left[\begin{array}{rrr|rrr}
		 2 & 0 & 6 & 1 & 0 & 0 \\
		-1 & 5 & 3 & 0 & 1 & 0 \\
		 1 & 3 & -1 & 0 & 0 & 1 \\
	\end{array}\right]

	\\

	\begin{array}{r}
		R_2 + (1/2)R_2 \\
		R_3 - (1/2)R_1
	\end{array}
	\left[\begin{array}{rrr|rrr}
		 2 & 0 & 6 & 1 & 0 & 0 \\
		 0 & 5 & 6 & 1/2 & 1 & 0 \\
		 0 & 3 & -2 & -1/2 & 0 & 1 \\
	\end{array}\right]

	\\

	\begin{array}{r}
		R_3 - (3/5)R_2
	\end{array}
	\left[\begin{array}{rrr|rrr}
		 2 & 0 & 6 & 1 & 0 & 0 \\
		 0 & 5 & 6 & 1/2 & 1 & 0 \\
		 0 & 0 & -28/5 & -4/5 & -3/5 & 1 \\
	\end{array}\right]

	\\

	\begin{array}{r}
		(1/2)R_1 \\
		(-5/28)R_3
	\end{array}
	\left[\begin{array}{rrr|rrr}
		 1 & 0 & 3 & 1/2 & 0 & 0 \\
		 0 & 5 & 6 & 1/2 & 1 & 0 \\
		 0 & 0 & 1 & 1/7 & 3/28 & -5/28 \\
	\end{array}\right]

	\\

	\begin{array}{r}
		R_1 - 3R_3 \\
		R_2 - 6R_3
	\end{array}
	\left[\begin{array}{rrr|rrr}
		 1 & 0 & 0 & 1/14 & -9/28 & 15/28 \\
		 0 & 5 & 0 & -5/14 & 5/14 & 15/14 \\
		 0 & 0 & 1 & 1/7 & 3/28 & -5/28 \\
	\end{array}\right]

	\\

	\begin{array}{r}
		(1/5)R_2
	\end{array}
	\left[\begin{array}{rrr|rrr}
		 1 & 0 & 0 & 1/14 & -9/28 & 15/28 \\
		 0 & 1 & 0 & -1/14 & 1/14 & 3/14 \\
		 0 & 0 & 1 & 1/7 & 3/28 & -5/28 \\
	\end{array}\right]

	\\

	A^{-1} = \begin{bmatrix}
		1/14 & -9/28 & 15/28 \\
		-1/14 & 1/14 & 3/14 \\
		 1/7 & 3/28 & -5/28 \\
	\end{bmatrix}
	= (1/28)
	\begin{bmatrix}
		2 & -9 & 15 \\
		-2 & 2 & 6 \\
		 4 & 3 & -5 \\
	\end{bmatrix}
\end{align}
$$

## Inverse of 2D Square Matrix

$$
A^{-1}
	= \dfrac{1}{ad - bc}
	  \begin{bmatrix} d & -b \\ -c & a\end{bmatrix}
$$

> [!warning]
> This is not applicable if $ad - bc = 0$

## Properties

| Property           | Statement                                   |
| ------------------ | ------------------------------------------- |
|                    | $(A^{-1})^{-1} = A$                         |
|                    | $(A^k)^{-1} = (A^{-1})^k$                   |
|                    | $(cA)^{-1} = \dfrac{1}{c} A^{-1}, c \neq 0$ |
|                    | $(A^{\top})^{-1} = (A^{-1})^{\top}$         |
|                    | $(AB)^{-1} = B^{-1}A^{-1}$                  |
| Right Cancellation | $AC = BC \rightarrow A = B$                 |
| Left Cancellation  | $CA = CB =\rightarrow A = B$                |

## Using Adjoint and Determinant

Assuming $A$ is an invertible square matrix, the inverse can be solved by taking the [[Matrix Adjoint]] and scaling it with the inverse of the matrix's [[Matrix Determinant|determinant]]

$$A^{-1} = \dfrac{1}{det(A)} Adj(A)$$

## References

1. Elementary Linear Algebra, Ch. 2, pp. 73-82
2. Elementary Linear Algebra, Ch. 3, pp. 159-160
3. Mathematics for Machine Learning, Ch.2, pp. 24-25
