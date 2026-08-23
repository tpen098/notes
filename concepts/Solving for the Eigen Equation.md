---
aliases: [Solving for the Eigen Equations]
tags: [linear-algebra]
date created: Wednesday, October 19th 2022, 5:58:32 pm
date modified: Friday, August 21st 2026, 2:59:21 pm
---

# Solving for the Eigen Equation

## Solving for the Eigen Spectrum

To obtain the [[Eigen Spectrum]] of a [Square Matrix](Matrix%20Special%20Types.md#Square%20Matrix) $A \in \mathbb{R}^{n \times n}$, simply find the roots of the [Characteristic Polynomial](Characteristic%20Polynomial.md).

$$
\begin{align}
p_A(\lambda) &:= det(A - \lambda I) = 0 \\
&:= c_0 + c_1 \lambda + c_2 \lambda^2 + \ldots + c_{n-1}\lambda_{n-1}+(-1)^n\lambda_n = 0 \\
\end{align}
$$

$$
S: \{\lambda_1, \lambda_2, \ldots, \lambda_{n-1}, \lambda_n \}
$$

## Solving for the Eigen Spaces

To solve for the [[Eigen Space]] of each [[Eigenvalue Equation|Eigenvalue]] $\lambda_i$ in the [[Eigen Spectrum]] solve for the [[Linear System General Solution]].

$$E_{\lambda_i}:A-\lambda I = 0$$

$$
E_{\lambda_i}:
\left[\begin{array}{rrrr|r}
	a_{11}-\lambda_i & a_{12} & \ldots & a_{1n} & 0 \\
	a_{21} & a_{22}-\lambda_i & \ldots & a_{2n} & 0 \\
	\vdots & \vdots & \ddots & \vdots & \vdots\\
	a_{m1} & a_{m2} & \ldots & a_{mn}-\lambda_i & 0 \\
\end{array}\right]
$$

> [!tip]
> Convert into [[Matrix Row Echelon Form]] and use the [[Minus 1 Trick]] last.

## Example

$$
A =
\dfrac{1}{2}
\begin{bmatrix}
	5 & -2 \\ -2 & 5
\end{bmatrix},
$$

### Eigen Spectrum

$$
det(A - \lambda I) =
\begin{vmatrix}
	\dfrac{5}{2} - \lambda & -1 \\
	-1 & \dfrac{5}{2} - \lambda \\
\end{vmatrix}
$$

$$
\left(\dfrac{5}{2} - \lambda\right)^2 - 1 = 0
$$

$$
\lambda_1 =\dfrac{7}{2}, \lambda_2=\dfrac{3}{2}
$$

### Eigen Spaces for First Eigen Value

$$
\begin{align}
Ap_1 &= \lambda_1 p_1 \\
\begin{bmatrix}
	\dfrac{5}{2} & -1 \\ -1 & \dfrac{5}{2} \\
\end{bmatrix}
&=
\dfrac{7}{2} p_1
\end{align}
$$

Reduce the augmented matrix into [[Matrix Row Echelon Form]]

$$
\begin{align}
\left[\begin{array}{rr|r}
	\dfrac{5}{2}-\dfrac{7}{2} & -1 & 0 \\
	-1 & \dfrac{5}{2}-\dfrac{7}{2} & 0\\
  \end{array}\right]
\\
\left[\begin{array}{rr|r}
	-1 & -1 & 0 \\
	-1 & -1 & 0\\
\end{array}\right]
\\
\left[\begin{array}{rr|r}
	1 & 1 & 0 \\
	1 & 1 & 0\\
\end{array}\right]
\\
\left[\begin{array}{rr|r}
	1 & 1 & 0 \\
	0 & 0 & 0\\
\end{array}\right]
\\
\begin{bmatrix}
	1 & 1 \\
	0 & \boxed{-1}\\
\end{bmatrix}
\end{align}
$$

$$p_1 = \begin{bmatrix} 1 \\ -1\end{bmatrix}$$

### Eigen Spaces for Second Eigen Value

$$
\begin{align}
Ap_2 &= \lambda_2 p_2 \\
\begin{bmatrix}
	\dfrac{5}{2} & -1 \\ -1 & \dfrac{5}{2} \\
\end{bmatrix}
&=
\dfrac{3}{2} p_2
\end{align}
$$

Reduce the augmented matrix into [[Matrix Row Echelon Form]]

$$
\begin{align}
\left[\begin{array}{rr|r}
	\dfrac{5}{2}-\dfrac{3}{2} & -1 & 0 \\
	-1 & \dfrac{5}{2}-\dfrac{3}{2} & 0\\
  \end{array}\right]
\\
\left[\begin{array}{rr|r}
	1 & -1 & 0 \\
	-1 & 1 & 0\\
\end{array}\right]
\\
\left[\begin{array}{rr|r}
	1 & -1 & 0 \\
	0 & 0 & 0\\
\end{array}\right]
\\
\begin{bmatrix}
	1 & -1 \\
	0 & \boxed{-1}\\
\end{bmatrix}
\end{align}
$$

$$p_2 =
\begin{bmatrix} -1 \\ -1\end{bmatrix}
\to
\begin{bmatrix} 1 \\ 1\end{bmatrix}
$$

## References

---

1. [[@Mathematics for Machine Learning]] (ch.4, pp. 105-107, 117-118)
2. [@Eigenvectors&Eigenvalues](https://www.youtube.com/watch?v=PFDu9oVAE-g&t=164s) (3blue1brown)
