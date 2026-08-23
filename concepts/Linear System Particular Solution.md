---
tags: [linear-algebra]
aliases: [Linear System Special Solution, Particular Solution, Particular Solutions, Special Solution, Special Solutions]
date created: Wednesday, October 19th 2022, 2:24:25 pm
date modified: Friday, August 21st 2026, 10:12:07 am
---

# Linear System Particular Solution

## Definition

The [[Linear System Particular Solution|Particular Solution]] or [[Linear System Particular Solution|Special Solutions]] of a [[Linear System]] is the variable column [[Vector Space|Vector]] that solves $Ax = b$

## Example

Given the [[Matrix]] above already in [[Matrix Row Reduced Row Echelon Form]]

$$
\begin{bmatrix}
	1 & 0 & 8 & -4 \\
	0 & 1 & 2 & 12 \\
\end{bmatrix}
\begin{bmatrix}
	x_1 \\ x_2 \\ x_3 \\ x_4
\end{bmatrix}
=
\begin{bmatrix}
	42 \\ 8
\end{bmatrix}
$$

The solution would be the following column [[Vector Space|Vector]]

$$
\begin{bmatrix}
	x_1 \\ x_2 \\ x_3 \\ x_4
\end{bmatrix}
=
\begin{bmatrix}
	42 \\ 8 \\ 0 \\ 0
\end{bmatrix}
$$

> [!tip] Empty Elements
> For empty or undefined elements, simply convert the element to zero

## References

1. Mathematics for Machine Learning, Ch.2, pp. 27-33
