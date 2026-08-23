---
aliases: []
tags: [linear-algebra]
date created: Wednesday, October 19th 2022, 2:25:03 pm
date modified: Friday, August 21st 2026, 2:10:12 pm
---

# Minus 1 Trick

## Description

A convenient method to generate all column vectors of the [[Linear System General Solution]].

> [!note] Preliminary Step
> Make sure the matrix is in [[Matrix Row Echelon Form]]

## Procedure

1. Augment the [[Matrix]] into a [[Square Matrix]] by inserting zero rows in between rows that skip a leading entry (if it were to follow the form of an [[Identity Matrix]]). If one more row needs to be added still, add one at the end.
2. For each added zero row, place a $-1$ value into its diagonal entry. At this point, the matrix should be square with original diagonal entries being $1$ and the inserted diagonal entries being $-1$
3. Simply take every column that has an changed $-1$ diagonal entry as the general solution column vectors

## Example

Consider the matrix below.

$$
\left[\begin{array}{rrrr|r}
	1 & 3 & 0 & 0 & 3 \\
	0 & 0 & 1 & 0 & 9 \\
	0 & 0 & 0 & 1 & -4 \\
\end{array}\right]
$$

Append after the first row and at the end to make the [[Linear System#Augmented Matrix Form|augmented matrix]] a $5\times 5$ Square Matrix.

$$
\left[\begin{array}{rrrr|r}
	1 & 3 & 0 & 0 & 3 \\
	0 & 0 & 1 & 0 & 9 \\
	0 & 0 & 0 & 1 & -4 \\
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr|r}
	1 & 3 & 0 & 0 & 3 \\
	0 & 0 & 0 & 0 & 0 \\
	0 & 0 & 1 & 0 & 9 \\
	0 & 0 & 0 & 1 & -4 \\
	0 & 0 & 0 & 0 & 0 \\
  \end{array}\right]
$$

Set the inserted rows to have a leading value of $-1$ in the entry where each diagonal entry will be filled.

$$
\left[\begin{array}{rrrr|r}
	1 & 3 & 0 & 0 & 3 \\
	0 & 0 & 0 & 0 & 0 \\
	0 & 0 & 1 & 0 & 9 \\
	0 & 0 & 0 & 1 & -4 \\
	0 & 0 & 0 & 0 & 0 \\
\end{array}\right]
\rightarrow
\left[\begin{array}{rrrr|r}
	1 & 3 & 0 & 0 & 3 \\
	0 & -1 & 0 & 0 & 0 \\
	0 & 0 & 1 & 0 & 9 \\
	0 & 0 & 0 & 1 & -4 \\
	0 & 0 & 0 & 0 & -1 \\
\end{array}\right]
$$

The general solution can now be obtained. Select all the columns that has a $-1$ leading entry due to step 2.

$$
x =
\lambda_1
\begin{bmatrix}
	3 \\ -1 \\ 0 \\ 0 \\ 0
\end{bmatrix}
\lambda_2
\begin{bmatrix}
	3 \\ 0 \\ 9 \\ -4 \\ -1
\end{bmatrix}
$$

> [!warning]
> Again, only take the column vectors that have a $-1$ leading entry because of step 2.

## References

1. Mathematics for Machine Learning, Ch.2, pp. 27-33
