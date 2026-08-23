---
aliases: [Rotations in 3D]
tags: ["", linear-algebra]
date created: Thursday, September 22nd 2022, 7:37:55 pm
date modified: Friday, August 21st 2026, 2:45:14 pm
---

# Rotation in 3D

## Statement

With respect to the following standard [[Basis]]

$$
\left \{
	e_1
	=
	\begin{bmatrix}
	1 \\ 0 \\ 0 \\
	\end{bmatrix},
	e_2
	=
	\begin{bmatrix}
	0 \\ 1 \\ 0 \\
	\end{bmatrix}
	e_3
	=
	\begin{bmatrix}
	0 \\ 0 \\ 1 \\
	\end{bmatrix}
\right\}
\text{ of } \mathbb{R}^3
$$

> [!NOTE] Intuition
> There are three [[Rotation]] [[Matrix|matrices]], one for every [[Basis]] such that the counter-clockwise rotation is performed on the plane encapsulated by the other bases while the considered basis is fixed in place.

## Rotation About the $e_1$ Axis

$$
R_1(\theta)
=
\begin{bmatrix}
	1 & 0 & 0 \\
	0 & \cos{\theta} & -\sin{\theta} \\
	0 & \sin{\theta} & \cos{\theta} \\
\end{bmatrix}
$$

## Rotation About the $e_2$ Axis

$$
R_2(\theta)
=
\begin{bmatrix}
	\cos{\theta} & 0 & \sin{\theta} \\
	0 & 1 & 0 \\
	-\sin{\theta} & 0 & \cos{\theta} \\
\end{bmatrix}
$$

## Rotation About the $e_3$ Axis

$$
R_3(\theta)
=
\begin{bmatrix}
	\cos{\theta} & -\sin{\theta} & 0 \\
	\sin{\theta} & \cos{\theta} & 0 \\
	0 & 0 & 1 \\
\end{bmatrix}
$$

## Generalization

The three rotation matrices can be generalized into one [[Transformation Matrix]] as follows

$$
	R = R_3 R_2 R_1
$$

> [!warning]
> Rotation matrices are not commutative in this case so mind the order of operation.

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 91-93
