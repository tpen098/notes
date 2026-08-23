---
aliases: [Solving for Singular Value Decompositions]
tags: [linear-algebra]
date created: Thursday, October 20th 2022, 10:21:15 am
date modified: Friday, August 21st 2026, 2:58:41 pm
---

# Solving for Singular Value Decomposition

## Conversion to a Symmetric, Positive Definite Matrix

Convert the given [[Matrix]] $A$ to a [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] $S$.

$$
S = A^{\top}A
$$

## Auxiliary Eigendecomposition

Perform [[Eigendecomposition]] on $S$

$$
S = PDP^{\top}
$$

## Singular Value Matrix Construction

The [[Singular Value Matrix]] is equal to the [[Diagonal Matrix]] $D$ except each element should be in square root: $\sigma_i = \sqrt{\lambda_i}$

> [!Note] Singular Value Matrix Dimensions
> If the [[Singular Value Matrix]] dimension is different from the [[Diagonal Matrix]], pad zero rows or columns accordingly.

## Right-Side Change of Basis $V$ Construction

The [[Matrix]] $V$ is simply equal to the [[Matrix]] $P$ from the [[Eigendecomposition]].

> [!warning] Calculate the Matrix Transposition of $V$
> The [[Matrix]] $V$ will be used to calculate for $U$ but the [[Singular Value Decomposition|SVD]] will use the [[Matrix Transpose]] of $V$ so calculate that as well.

## Left-Side Change of Basis $U$ Construction

Each column $u_i$ of $U$ is defined as the following

$$
u_i = \dfrac{1}{\sigma_i} Av_i
$$

## Example

$$
A =
\begin{bmatrix}
	1 & 0 & 1 \\ -2 & 1 & 0
\end{bmatrix}
$$

### Conversion to a Symmetric, Positive Definite Matrix

$$
A^{\top}A =
\begin{bmatrix}
	1 & -2 \\ 0 & 1 \\ 1 & 0
\end{bmatrix}
\begin{bmatrix}
	1 & 0 & 1 \\ -2 & 1 & 0
\end{bmatrix}
=
\begin{bmatrix}
	5 & -2 & 1 \\
	-2 & 1 & 0 \\
	1 & 0 & 1
\end{bmatrix}
$$

### Auxiliary Eigendecomposition

$$
A^{\top}A = PDP^{\top} =
\begin{bmatrix}
	\dfrac{5}{\sqrt{30}} & 0 & -\dfrac{1}{\sqrt{6}} \\
	-\dfrac{2}{\sqrt{30}} & \dfrac{1}{\sqrt{5}} & -\dfrac{2}{\sqrt{6}} \\
	\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{5}} & \dfrac{1}{\sqrt{6}}
\end{bmatrix}
\begin{bmatrix}
	6 & 0 & 0 \\
	0 & 1 & 0 \\
	0 & 0 & 0
\end{bmatrix}
{
\begin{bmatrix}
	\dfrac{5}{\sqrt{30}} & 0 & -\dfrac{1}{\sqrt{6}} \\
	-\dfrac{2}{\sqrt{30}} & \dfrac{1}{\sqrt{5}} & -\dfrac{2}{\sqrt{6}} \\
	\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{5}} & \dfrac{1}{\sqrt{6}}
\end{bmatrix}
}^{\top}
$$

### Right-Side Change of Basis $V$ Construction

$$
V = P =
\begin{bmatrix}
	\dfrac{5}{\sqrt{30}} & 0 & -\dfrac{1}{\sqrt{6}} \\
	-\dfrac{2}{\sqrt{30}} & \dfrac{1}{\sqrt{5}} & -\dfrac{2}{\sqrt{6}} \\
	\dfrac{1}{\sqrt{30}} & \dfrac{2}{\sqrt{5}} & \dfrac{1}{\sqrt{6}}
\end{bmatrix}
$$

### Singular Value Matrix Construction

$$
D \to \Sigma =
\begin{bmatrix}
	\sqrt{6} & 0 & 0 \\
	0 & \sqrt{1} & 0 \\
\end{bmatrix}
$$

### Left-Side Change of Basis $U$ Construction

$$
\begin{align}
u_1 &= \dfrac{1}{\sigma_1} Av_1
=
\dfrac{1}{\sigma_1}
\begin{bmatrix}
	1 & 0 & 1 \\ -2 & 1 & 0
\end{bmatrix}
\begin{bmatrix}
	\dfrac{5}{\sqrt{30}} \\
	-\dfrac{2}{\sqrt{30}} \\
	\dfrac{1}{\sqrt{30}} \\
\end{bmatrix}
=\begin{bmatrix}
	\dfrac{1}{\sqrt{5}} \\ -\dfrac{2}{\sqrt{5}}
\end{bmatrix}
\\
u_2 &= \dfrac{1}{\sigma_2} A v_2
=
\dfrac{1}{\sigma_1}
\begin{bmatrix}
	1 & 0 & 1 \\ -2 & 1 & 0
\end{bmatrix}
\begin{bmatrix}
	0 \\
	-\dfrac{1}{\sqrt{5}} \\
	\dfrac{2}{\sqrt{5}} \\
\end{bmatrix}
=
\begin{bmatrix}
	\dfrac{2}{\sqrt{5}} \\ \dfrac{1}{\sqrt{5}}
\end{bmatrix}
\\
U &=
\begin{bmatrix}
	\dfrac{1}{\sqrt{5}} & \dfrac{2}{\sqrt{5}} \\
	-\dfrac{2}{\sqrt{5}} & \dfrac{1}{\sqrt{5}} \\
\end{bmatrix}
\end{align}
$$

## References

1. Mathematics for Machine Learning, Ch.4, pp. 122-127
