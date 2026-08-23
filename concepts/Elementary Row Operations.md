---
tags: [linear-algebra]
aliases: [Elementary Row Operation]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Thursday, August 20th 2026, 6:25:05 pm
---

# Elementary Row Operations

## Matrix Invariance

Any pair of rows in the [[Matrix|matrix]] can be applied an [[Elementary Row Operations|Elementary Row Operation]] without changing the original system of equations

## Interchange Any Rows

$$
\begin{align*}
	&\left[\begin{array}{rrr|r}
		a_{11} & a_{12} & a_{13} & b_1\\
		a_{21} & a_{22} & a_{23} & b_2\\
		a_{31} & a_{32} & a_{33} & b_3\\
	\end{array}\right]
	\\
	R_1 \leftrightarrow R_3
	&\left[\begin{array}{rrr|r}
		a_{31} & a_{32} & a_{33} & b_3 \\
		a_{21} & a_{22} & a_{23} & b_2 \\
		a_{11} & a_{12} & a_{13} & b_1 \\
  \end{array}\right]
\end{align*}
$$

## Multiply a Row by a Nonzero Constant

$$
\begin{align*}
	&\left[\begin{array}{rrr|r}
		a_{11} & a_{12} & a_{13} & b_1\\
		a_{21} & a_{22} & a_{23} & b_2\\
		a_{31} & a_{32} & a_{33} & b_3\\
	\end{array}\right]
	\\
	kR_2
	&\left[\begin{array}{rrr|r}
		a_{11} & a_{12} & a_{13} & b_1 \\
		k a_{21} & k a_{22} & k a_{23} & k b_2 \\
		a_{31} & a_{32} & a_{33} & b_3 \\
  \end{array}\right]
\end{align*}
$$

## Add a Multiple of a Row to Another Row

$$
\begin{align*}
	&\left[\begin{array}{rrr|r}
		a_{11} & a_{12} & a_{13} & b_1\\
		a_{21} & a_{22} & a_{23} & b_2\\
		a_{31} & a_{32} & a_{33} & b_3\\
	\end{array}\right]
	\\
	R_3 + g R_2
	&\left[\begin{array}{rrr|r}
		a_{11} & a_{12} & a_{13} & b_1 \\
		a_{21} & a_{22} & a_{23} & b_2 \\
		a_{31} + g a_{21} & a_{32} + g a_{22} & a_{33} + g a_{23} & b_3 + g b_2 \\
  \end{array}\right]
\end{align*}
$$

## References

1. Elementary Linear Algebra, Ch. 1 pp. 15-18
