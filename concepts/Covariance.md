---
aliases: [Covariances, Covariance Matrix, Covariance Matrices]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 2:52:29 pm
date modified: Sunday, August 16th 2026, 11:20:58 pm
---
33
# Covariance

## Univariate Definition

The [[Covariance]] between two univariate [[Random Variable|Random Variables]] $X, Y \in \mathbb{R}$ is given by the expected product of their deviations from their respective means as shown

$$
Cov_{X, Y}[x, y] := \mathbb{E}_{X, Y}
[(x-\mathbb{E}_{X}[x])(x-\mathbb{E}_{Y}[y])]
$$

Using the linearity of [[Expected Value|Expectations]], the definition can be rewritten as the [[Expected Value]] of the products minus the product of the [[Mean|Means]] as shown

$$
Cov_{X, Y}
= \mathbb{E}_{X, Y} [xy]
- \mathbb{E}_{X} [x] \mathbb{E}_{Y} [y]
$$

## Multivariate Definition

The [[Covariance]] between two multivariate [[Random Variable|Random Variables]] $X \in \mathbb{R}^D, Y \in \mathbb{R}^E$ can be defined using [[Matrix Transpose]] as shown in the following

$$
\begin{align}
Cov[x, y]
&= \mathbb{E}_{X, Y}
[(x-\mathbb{E}_{X}[x])(x-\mathbb{E}_{Y}[y])^{\top}] \\
&= \mathbb{E}_{X, Y} [xy^{\top}]
- \mathbb{E}_{X} [x] \mathbb{E}_{Y} [y]^{\top} \\
&= Cov[y, x]^{\top}
\end{align}
$$

## Covariance Matrix

 Alternatively, the [[Covariance]] between two multivariate [[Random Variable|Random Variables]] $X \in \mathbb{R}^D, Y \in \mathbb{R}^E$ can be defined using a [[Symmetric Positive Definite]] [[Matrix]] known as the [[Covariance|Covariance Matrix]] as shown below

$$
Cov_{X, Y}[x, y] =
\begin{bmatrix}
Cov[x_{1}, y_{1}] & \dots & Cov[x_{1}, y_{E}] \\
\vdots & \ddots & \vdots \\
Cov[x_{D}, y_{1}] & \dots & Cov[x_{D}, y_{E}]
\end{bmatrix}
$$

## Covariance of an Affine Transformation

Given a [[Random Variable]] $X$ with an Affine Transformation $y = Ax + b$, the [[Covariance]] is defined as the following

$$
\begin{align}
Cov[x, y]
&= \mathbb{E}[x(Ax+b)^{\top}]
- \mathbb{E}[x]\mathbb{E}[Ax+b]^{\top} \\
&= \mathbb{E}[x]b^{\top}
+ \mathbb{E}[xx^{\top}] A^{\top}
- \mu b^{\top}
- \mu \mu^{\top}A^{\top} \\
&= \mu b^{\top} - \mu b^{\top}
+ (\mathbb{E}[xx^{\top}] - \mu \mu^{\top})A^{\top} \\
&= \mathbb{V}_{X}[x]A^{\top}
\end{align}
$$

> [!NOTE] Bias
> The Bias of the Affine Transformation doesn't affect the final [[Covariance]]

## References

1. Mathematics for Machine Learning, pp. 187-191, 194
