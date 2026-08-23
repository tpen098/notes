---
aliases: [Elementary Transformation]
tags: [linear-algebra]
date created: Thursday, September 15th 2022, 2:40:55 pm
date modified: Thursday, August 20th 2026, 6:26:03 pm
---

# Elementary Transformations

## Gaussian Elimination

1. Find the leftmost nonzero column of the [[Matrix|matrix]]
2. If the pivot is not on the first row then interchange rows to bring it to the top
3. Add suitable multiples of the first row to the rows below it to turn all entries below the pivot to zero
4. Ignore this row and redo the process for rows below until the matrix is in [[Matrix Row Echelon Form]]

### Example

$$
\begin{align*}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		 -1 & -2 & 3 & 1 \\
		  3 & -7 & 4 & 10 \\
	\end{array}\right] \\

	\begin{array}{r}
		R_2 + R_1 \\
		R_3 - 3 R_1 \\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		  0 & -1 & 5 & 9 \\
		  0 & -10 & -2 & -14 \\
	\end{array}\right] \\

	\begin{array}{r}
		- R_2\\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		  0 & 1 & -5 & -9 \\
		  0 & -10 & -2 & -14 \\
	\end{array}\right] \\

	\begin{array}{r}
		R_3 + 10 R_2 \\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		  0 & 1 & -5 & -9 \\
		  0 & 0 & -52 & -104 \\
	\end{array}\right] \\

	\begin{array}{r}
		- \dfrac{1}{52} R_3 \\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		  0 & 1 & -5 & -9 \\
		  0 & 0 & 1 & 2 \\
	\end{array}\right] \\
\end{align*}
$$

## Gauss-Jordan Reduction

1. Perform gaussian , except make sure that the leading entries are 1 via [[Elementary Row Operations#Multiply a Row by a Nonzero Constant|scaling]] to turn the matrix into [[Matrix Row Reduced Row Echelon Form]]
2. For each row from the bottom, add a multiple of the bottom row to the upper rows to turn non-leading entries to zero

### Example

$$
\begin{align*}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 2 & 8 \\
		  0 & 1 & -5 & -9 \\
		  0 & 0 & 1 & 2 \\
	\end{array}\right] \\

	\begin{array}{r}
		R_2 + 5 R_3 \\
		R_1 - 2 R_3 \\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 1 & 0 & 4 \\
		  0 & 1 & 0 & 1 \\
		  0 & 0 & 1 & 2 \\
	\end{array}\right] \\

	\begin{array}{r}
		R_1 - 1 R_2 \\
	\end{array}
	&\left[\begin{array}{rrr|r}
		  1 & 0 & 0 & 3 \\
		  0 & 1 & 0 & 1 \\
		  0 & 0 & 1 & 2 \\
	\end{array}\right] \\

\end{align*}
$$

## References

1. Elementary Linear Algebra, Ch. 1, pp. 1-10, 14-15, 19-24)
2. Elementary Linear Algebra, Ch. 2, pp. 53-56, 83-84)
3. Mathematics for Machine Learning, Ch.2, pp. 22-23)
