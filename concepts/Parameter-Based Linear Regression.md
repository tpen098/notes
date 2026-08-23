---
aliases: [Parameter-Based Linear Regression Problem, Parameter-Based Linear Regression Problems, Parameter-Based Linear Regressions]
tags: [statistics-probability, machine-learning]
date created: Saturday, November 26th 2022, 11:59:22 am
date modified: Friday, August 21st 2026, 2:22:37 pm
---

# Parameter-Based Linear Regression

## Non-Featured Model Representation

The goal of [[Parameter-Based Linear Regression]] is to find parameters $\theta$ of a [[Function]] [[Machine Learning Model|Model]] $f$ that maps the [[Domain]] $x \in \mathbb{R}^D$ to [[Codomain]] $f(x) \in \mathbb{R}$ assuming a [[Dataset]] wherein $y_{n} = f(x_{n}) + \epsilon$. The $\epsilon$ term is a [[Independent and Identically Distributed|IID]] [[Random Variable]] that describes the measurement noise and potentially unmodelled processes.

$$
y = f(x) + \epsilon
$$

Alternatively, for a [[Gaussian Distribution|Normal Distribution]] Noise with Zero [[Mean]], the [[Machine Learning Model|Model]] can be interpreted as a [[Conditional Gaussian Distribution]] given input $x$

$$
p(y|x) = \mathcal{N}(y|f(x), \sigma^{2})
\atop
y =
x^{\top}\theta + \epsilon,
\epsilon = \mathcal{N}(0, \sigma^2)
$$

The collection of all [[Model Input|Model Inputs]] $x$ can be defined using the Design [[Transformation Matrix]] $X$

$$
X
:= [x_{1}, \dots, x_{N}]^{\top} \in \mathbb{R}^{N\times D}
$$

## Parameter Estimation

Given a [[Parameter-Based Linear Regression]] setting with a given [[Dataset]], the [[Bayes' Theorem|Likelihood function]] for [[Codomain]] $\mathcal{Y}$ is defined as shown

$$
\begin{align}
p(\mathcal{Y}|\mathcal{X}, \theta)
&= p(y_{1}, \dots, y_{N}|x_{1}, \dots, x_{N}, \theta) \\
&= \prod_{n=1}^{N} p(y_{n}|x_{n}, \theta) \\
&= \prod_{n=1}^{N} \mathcal{N}(y_{n}|x_{n}^{\top}\theta, \sigma^2) \\
\end{align}
$$

The parameters $\theta$ must maximize the [[Bayes' Theorem|Likelihood Function]] to minimize the [[Loss Function|Loss]]

$$
\theta_{ML}
= \arg \max_{\theta}
  p(\mathcal{Y}|\mathcal{X},\theta) \in \mathbb{R}^D
$$

## Featured Model Representation

For nonlinearf [[Function|Functions]], an arbitrary nonlinear transformation $\phi: \mathbb{R}^D \to \mathbb{R}^K$ can be applied for [[Domain]] $x \in \mathbb{R}^D$ to retain the [[Linear Combination]]. This changes the [[Machine Learning Model|Model]] [[Function]] and [[Probability]] [[Bayes' Theorem|Likelihood Function]] to the following

$$
\begin{align}
p(y|x, \theta)
&= \mathcal{N}(y|\phi ^{\top}(x)\theta, \sigma^2) \\
\Longleftrightarrow
\phi ^{\top}(x)\theta + \epsilon
&= \sum_{k=0}^{K-1}\theta_{k}\phi_{k}(x)+\epsilon
\end{align}
$$

The collection of the nonlinear transformation $\phi$ on all [[Model Input|Model Inputs]] $x$ can be defined using the Design [[Matrix]] $\Phi$

$$
\Phi
:=
\begin{bmatrix}
\phi ^{\top}(x_{1}) \\ \vdots \\ \phi ^{\top}(x_{N})
\end{bmatrix}
=
\begin{bmatrix}
\phi_{0}(x_{1}) & \dots & \phi_{k-1}(x_{1}) \\
\vdots & \ddots & \vdots \\
\phi_{0}(x_{N}) & \dots & \phi_{k-1}(x_{N}) \\
\end{bmatrix}
\in \mathbb{R}^{N \times K}
$$

The parameter vector $\theta$ that best approximates the [[Machine Learning Model|Model]] or provides the [[Machine Learning Model|Model]] [[Codomain]] with minimal [[Loss Function|Loss]] is determined via [[Unconstrained Optimization]] or [[Constrained Optimization]] techniques on Statistical Learning Theories

## References

1. Mathematics for Machine Learning, pp. 289-315
