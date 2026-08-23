---
aliases: [Gaussian Distributions, Normal Distribution, Gaussian, Normal, Gaussians]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 7:31:45 pm
date modified: Thursday, August 20th 2026, 6:55:24 pm
---

# Gaussian Distribution

## Univariate Probability Density Function

A continuous, univariate [[Random Variable]] with a [[Gaussian Distribution]] has the following [[Probability Density Function]]

$$
p(x|\mu, \sigma^2)
= \frac{1}{\sqrt{ 2\pi \sigma^2 }}
\exp\left( -\frac{(x-\mu)^2}{2\sigma^2} \right)
$$

Where $\mu \in \mathbb{R}$ is the [[Mean]], and $\sigma^2 \in \mathbb{R}$ is the [[Standard Deviation]] squared, or the [[Variance]].

## Multivariate Probability Density Function

A continuous, multivariate [[Random Variable]] with a [[Gaussian Distribution]] has the following [[Probability Density Function]]

$$
p(x|\mu, \Sigma) =
(2\pi)^{-D/2}
\lvert \Sigma \rvert^{-1/2}
\exp\left( -\frac{1}{2}(x-\mu)^{\top}\Sigma^{-1})(x-\mu) \right)
$$

Where $\mu \in \mathbb{R}^D$ is the [[Mean]] vector, and $\Sigma$ is the [[Covariance|Covariance Matrix]] of the [[Random Variable]] with itself.

## Notation

The [[Probability Density Function]] can be written as follows

$$
p(x) \sim \mathcal{N}(x|\mu, \Sigma)
\atop
p(X) \sim \mathcal{N}(\mu, \Sigma)
$$

## Exponential Family Representation

Consider a univariate [[Gaussian Distribution]] $\mathcal{N}(x|\mu, \sigma^2)$ and a [[Fisher-Neyman Theorem|Sufficient Statistic]] as shown

$$
\phi(x) =
\begin{bmatrix}
x \\ x^2 \\
\end{bmatrix}
$$

Then the [[Gaussian Distribution]] can be defined as member of the [[Exponential Family]] as shown in the following

$$
\begin{align}
p(x|\theta)
&\propto \exp(\theta_{1}x+\theta_{2}x)
\\
\theta
&= \begin{bmatrix}
\dfrac{\mu}{\sigma^2} \\ \dfrac{-1}{2 \sigma^2}
\end{bmatrix}
\\
p(x|\theta)
&\propto \exp
\left(\dfrac{x\mu}{\sigma^2}
- \dfrac{x^2}{2 \sigma^2} \right)
&\propto \exp
\left(-\dfrac{1}{2\sigma^2} (x-\mu)^2 \right)
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 198-204, 212
