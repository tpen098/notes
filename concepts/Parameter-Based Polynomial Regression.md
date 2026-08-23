---
aliases: [Parameter-Based Polynomial Regressions]
tags: [machine-learning]
date created: Saturday, November 26th 2022, 5:42:52 pm
date modified: Friday, August 21st 2026, 2:26:46 pm
---

# Parameter-Based Polynomial Regression

## Model Definition

A [[Parameter-Based Polynomial Regression]] is a special case of a Featured [[Parameter-Based Linear Regression]] $y = \phi ^{\top}(x)\theta+\epsilon$ with [[Model Input|Feature]] $x \in \mathbb{R}$ and parameters $\theta \in \mathbb{R}^K$. The transformation $\phi(x)$ often defined as the following

$$
\phi(x)
=
\begin{bmatrix}
\phi_{0}(x) \\
\phi_{1}(x) \\
\phi_{2}(x) \\
\phi_{3}(x) \\
\vdots \\
\phi_{K-1}(x) \\
\end{bmatrix}
=
\begin{bmatrix}
1 \\ x \\ x^2 \\ x^3 \\ \vdots \\ x^{K-1}
\end{bmatrix}
\in \mathbb{R}^{K}
$$

Thus, the [[Machine Learning Model|Model]] is a [[Linear Combination]] of monomials of increasing degree

$$
f(x) = \sum_{k=0}^{K-1} \theta_{k}x^k = \phi ^{\top}(x)\theta
$$

## Multivariate Model Definition

For a given [[Dataset]] with $0, \dots, N-1$ [[Model Input|Model Inputs]] $x$, the Design [[Matrix]] $\Phi$ is used

$$
\Phi
:=
\begin{bmatrix}
\phi_{0} ^{\top}(x_{0}) \\
\phi_{1} ^{\top}(x_{1}) \\
\phi_{2} ^{\top}(x_{2}) \\
\phi_{3} ^{\top}(x_{3}) \\
\vdots \\
\phi ^{\top}(x_{N})
\end{bmatrix}
=
\begin{bmatrix}
\phi_{0}(x_{0}) & \dots & \phi_{K-1}(x_{0}) \\
\phi_{0}(x_{1}) & \dots & \phi_{K-1}(x_{1}) \\
\phi_{0}(x_{2}) & \dots & \phi_{K-1}(x_{2}) \\
\phi_{0}(x_{3}) & \dots & \phi_{K-1}(x_{3}) \\
\vdots & \ddots & \vdots \\
\phi_{0}(x_{N-1}) & \dots & \phi_{K-1}(x_{N-1}) \\
\end{bmatrix}
\in \mathbb{R}^{N \times K}
$$

Thus, the [[Machine Learning Model|Model]] can be expressed as the [[Matrix Multiplication]] of the Design [[Matrix]] and the parameter vector. The parameter vector can be substituted with its optimized form using [[Parameter-Based Linear Regression (MAP)]] or [[Parameter-Based Linear Regression (MLE)]] application as shown

$$
\begin{align}
f
&= \Phi\theta \\
&\approx \Phi (\Phi^{\top}\Phi)^{-1} \Phi^{\top} y \\
&\approx \Phi \left( \Phi ^{\top}\Phi+\frac{\sigma^2}{b^2}I \right)^{-1} \Phi ^{\top} y \\
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 295-299, 302
