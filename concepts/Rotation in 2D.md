---
aliases: [Rotations in 2D]
tags: [linear-algebra]
date created: Sunday, August 16th 2026, 1:17:07 pm
date modified: Friday, August 21st 2026, 2:44:47 pm
---

# Rotation in 2D

## Statement

With respect to the following standard [[Basis]]

$$
\left \{ 
	e_1 
	= 
	\begin{bmatrix} 
	1 \\ 0 \\
	\end{bmatrix},
	e_2
	= 
	\begin{bmatrix} 
	0 \\ 1 \\
	\end{bmatrix}
\right\}
\text{ of } \mathbb{R}^2
$$

The following [[Rotation]] [[Matrix|matrix]] performs a [[Basis Change]] into the rotated coordinates $R(\theta)$

$$
R(\theta)
=
\begin{bmatrix}
	\cos{\theta} & -\sin{\theta} \\
	\sin{\theta} & \cos{\theta} \\
\end{bmatrix}
$$

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 91-92
