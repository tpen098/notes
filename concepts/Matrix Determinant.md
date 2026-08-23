---
aliases: [Matrix Determinants, Determinant, Determinants]
tags: [linear-algebra]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 1:24:12 pm
---

# Matrix Determinant

## Recursive Definition Using Cofactor or Laplace Expansion

Let $A$ be a [[Square Matrix]]. The [[Matrix Determinant]] of $A$ is recursively defined as the following

$$
		det(A) = |A| = \sum_{j=1}^n (-1)^{(1+j)} a_{1j} M_{1j}
$$

where $M_{ij}$, the minor of the element $a_{ij}$, is the determinant of matrix $A$ if the $ith$ row and $jth$ column were removed

> [!note] Cofactor
> The $C_{ij} = (-1)^{(i+j)} M_{ij}$ is called the **cofactor** of element $a_{ij}$

### First Order

$$
A = \begin{bmatrix}
	a_{11}
\end{bmatrix}
$$

$$
det(A) = a_{11}
$$

### Second Order

$$
A = \begin{bmatrix}
	a_{11} & a_{12} \\
	a_{21} & a_{22} \\
\end{bmatrix}
$$

$$
\begin{align}
det(A)
&= a_{11}A_{11} - a_{12}A_{12} \\
&= a_{11}a_{22} - a_{12}a_{21}
\end{align}
$$

### Third Order

$$
A = \begin{bmatrix}
	a_{11} & a_{12} & a_{13} \\
	a_{21} & a_{22} & a_{23} \\
	a_{31} & a_{32} & a_{33} \\
\end{bmatrix}
$$

$$
\begin{align}
	det(A)
	&= a_{11}A_{11} - a_{11}A_{11} + a_{11}A_{11} \\
	&= a_{11}
		\begin{vmatrix} a_{22} & a_{23} \\ a_{32} & a_{33} \end{vmatrix}
		-a_{12}
		\begin{vmatrix} a_{21} & a_{23} \\ a_{31} & a_{33} \end{vmatrix}
		+a_{13}
		\begin{vmatrix} a_{21} & a_{22} \\ a_{31} & a_{32} \end{vmatrix} \\
	&= a_{11} (a_{22}a_{33} - a_{23}a_{32})
		- a_{12} (a_{21}a_{33} - a_{23}a_{31})
		+ a_{13} (a_{21}a_{32} - a_{22}a_{31})

\end{align}
$$

## Properties

1. $det(A^{\top}) = det(A)$
2. $det(A) = 0$ if it has a zero column or zero row
3. $det(A) = 0$ if it has two identical columns or rows
4. $det(AB) = det(A)det(B)$ if both are square matrices or A is an [[Elementary Matrix]]
5. $det(A^{-1}) = \dfrac{1}{det(A)}$ if A is invertible
6. The determinant is invariant to the choice of a [Basis](Basis.md) of a [Linear Mapping](Linear%20Mapping.md)

### Row Operation

#### Interchange Any Rows

With the row operation: [[Elementary Row Operations#Interchange Any Rows|Interchanging of rows]]

$$det(B) = -det(A)$$

#### Multiply a Row by a Nonzero Constant

With the row operation: [[Elementary Row Operations#Multiply a Row by a Nonzero Constant|Multiplying a Row by a Nonzero Constant]]

$$det(B) = kdet(A)$$

#### Add a Multiple of a Row to Another Row

With the row operation: [[Elementary Row Operations#Add a Multiple of a Row to another Row|Adding a multiple of a row to another row]]

$$ det(B) = det(A) $$

## Laplace Expansion Theorem

The [[Matrix Determinant|Determinant]] can be computed using any row or column (as opposed to just using the first row in the previous examples)

$$
\begin{align}
det(A)
	&= a_{i1} A_{i1} - a_{i2} A_{i2} + \ldots \\
	&= a_{1j} A_{1j} - a_{2j} A_{2j} + \ldots
\end{align}
$$

> [!tip]
> Choose the row or column with the most number of zero entries for easier calculations.

### Matrix Determinant by Row

Let $A = [a_{ij}] \in M_{n \times n} (\mathbb{R})$. The determinant of [[Matrix|matrix]] $A$ is recursively defined with row $x$ as the following

$$
		det(A) = |A| = \sum_{j=1}^n (-1)^{x+j} a_{xj} M_{xj}
$$

### Matrix Determinant by Column

Let $A = [a_{ij}] \in M_{n \times n} (\mathbb{R})$. The determinant of [[Matrix|matrix]] $A$ is recursively defined with column $y$ as the following

$$
		det(A) = |A| = \sum_{i=1}^n (-1)^{i+y} a_{iy} M_{iy}
$$

## Row Echelon Form Shortcut

If the matrix is in [[Matrix Row Echelon Form]], then the determinant is the product of all the leading entries, with some additional rules
1. Multiply the determinant by $(-1)^n$ where $n$ is the number of row swaps done
2. Divide the determinant by all row scaling done

### Example

$$
\begin{align*}
	&=
	\begin{vmatrix}
		  0 & 0 & 4 & -7 \\
		  3 & 4 & 1 & 7 \\
		 -2 & -2 & 1 & 0 \\
		  2 & 2 & 0 & 4 \\
	\end{vmatrix}
	\\
	&=
	(-1)
	\begin{vmatrix}
		  2 & 2 & 0 & 4 \\
		  3 & 4 & 1 & 7 \\
		 -2 & -2 & 1 & 0 \\
		  0 & 0 & 4 & -7 \\
	\end{vmatrix}
	[R_1 \leftrightarrow R_4]
	\\
	&=
	(-1)(2)
	\begin{vmatrix}
		  1 & 1 & 0 & 2 \\
		  3 & 4 & 1 & 7 \\
		 -2 & -2 & 1 & 0 \\
		  0 & 0 & 4 & -7 \\
	\end{vmatrix}
	\left[ \dfrac{1}{2} R_1 \right]
	\\
	&=
	(-1)(2)
	\begin{vmatrix}
		  1 & 1 & 0 & 2 \\
		  0 & 1 & 1 & 1 \\
		  0 & 0 & 1 & 4 \\
		  0 & 0 & 4 & -7 \\
	\end{vmatrix}
	[R_2 - 3 R_1, R_3 + 2R_1]
	\\
	&=
	(-1)(2)
	\begin{vmatrix}
		  1 & 1 & 0 & 2 \\
		  0 & 1 & 1 & 1 \\
		  0 & 0 & 1 & 4 \\
		  0 & 0 & 0 & -23 \\
	\end{vmatrix}
	[R_4 - 4R_3]
	\\
	&= (-1)^1(2)(1)(1)(1)(-23) = 46
\end{align*}
$$

## Definition Using Eigenvalues

The [[Matrix Determinant|Determinant]] of a [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $A \in \mathbb{R}^{n \times n}$ is defined as the product of its [Eigenvalues](Eigenvalue%20Equation.md) as shown in the following.

$$
det(A) = \prod_{i=1}^{n}\lambda_i
$$

## References

1. Elementary Linear Algebra, Ch. 3, pp. 122-148
2. Mathematics for Machine Learning, Ch.4, pp. 99, 112
