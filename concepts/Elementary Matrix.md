---
tags: [linear-algebra]
aliases: [Elementary Matrices]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Thursday, August 20th 2026, 6:24:27 pm
---

# Elementary Matrix

## Definition

An [[Elementary Matrix]] is an [[Identity Matrix]] with one applied [[Elementary Row Operations|Elementary Row Operation]]

> [!info]
> The [[Identity Matrix]] is, by definition, an [[Elementary Matrix]].

## Swapped Rows

$$
R_1 \leftrightarrow R_3
\begin{bmatrix}
	0 & 0 & 1 \\
	0 & 1 & 0 \\
	1 & 0 & 0 \\
\end{bmatrix}
$$

## Scaled Row

$$
(10 R_2)
\begin{bmatrix}
	1 & 0 & 0 \\
	0 & 10 & 0 \\
	0 & 0 & 1 \\
\end{bmatrix}
$$

## Adding a Multiple of a Row to Another Row

$$
R_2 + 3 R_1
\begin{bmatrix}
	1 & 0 & 0 \\
	3 & 1 & 0 \\
	0 & 0 & 1 \\
\end{bmatrix}
$$

## Properties

### Representation in Products

Let $A, B$ be [[Square Matrix|Square Matrices]]. If $B$ is obtained from $A$ by applying one [[Elementary Row Operations|Elementary Row Operation]]:

$$B = EA$$

## References

1. Elementary Linear Algebra, Ch. 2 pp. 87-88
