---
aliases: []
tags: [statistics-probability]
date created: Wednesday, November 9th 2022, 10:33:26 pm
date modified: Friday, August 21st 2026, 2:13:57 pm
---

# Multivariate Change of Variable Technique

## Probability Density Function

Let $f(x)$ be the [[Probability Density Function]] of a multivariate, continuous [[Random Variable]] $X$. If the vector-valued [[Function]] $y=U(x)$ is differentiable and invertible for all values of $x$, then for corresponding values of $y$, the [[Probability Density Function]] $Y = U(X)$ is given as the following

$$
f(y) =
f_{x}(U^{-1}(y))
\cdot
\left\lvert
\det\left(
\frac{ \partial }{ \partial y } U^{-1}(y) \right)
\right\rvert
$$

## Example

Consider a [[Random Variable]] $X$ with the following states

$$
x = \begin{bmatrix}
x_{1}\\ x_{2}
\end{bmatrix}
$$

with the following [[Probability Density Function]]

$$
f \left(
\begin{bmatrix}
x_{1}\\ x_{2}
\end{bmatrix}
\right)
=
\frac{1}{2\pi} \exp
\left(
- \frac{1}{2}
\begin{bmatrix}
x_{1}\\ x_{2}
\end{bmatrix}^{\top}
\begin{bmatrix}
x_{1}\\ x_{2}
\end{bmatrix}
\right)
$$

For a [[Linear Mapping|Linear Transformation]] with [[Matrix]] $A$ defined as shown

$$
A =
\begin{bmatrix}
a & b \\ c & d \\
\end{bmatrix},
A^{-1} =
\frac{1}{ad-bc}
\begin{bmatrix}
d & -b \\ -c & a \\
\end{bmatrix}
$$

The [[Random Variable]] of interest $Y$, with states formed as $y = Ax$ can be obtained using the [[Multivariate Change of Variable Technique]].

$$
f(x)
= f(A^{-1}y)
= \frac{1}{2\pi} \exp\left( -\frac{1}{2} \right)y^{\top} A^{-\top} A^{-1}y
$$

The [[Partial Derivative]] of a [[Matrix]] by a vector with respect to a vector is included in the [[Matrix Gradient Identities]]

$$
\det\left\lvert
\frac{ \partial }{ \partial y } A^{-1}y
\right\rvert
=\det \lvert A^{-1} \rvert
=\left\lvert \frac{1}{ad-bc} \right\rvert
$$

The final solution can then be evaluated as shown

$$
\begin{align}
f(y)
&= f(x) \left\lvert
\frac{ \partial }{ \partial y } A^{-1}y \right\rvert \\
&= \frac{1}{2\pi} \exp\left( -\frac{1}{2} \right)y^{\top} A^{-\top} A^{-1}y
\lvert ad - bc \rvert^{-1}
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 219-221
