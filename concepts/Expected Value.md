---
aliases: [Expected Values, Expectation, Expectations]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 2:08:24 pm
date modified: Thursday, August 20th 2026, 6:46:21 pm
---

# Expected Value

## Univariate Continuous Definition

The [[Expected Value]] of a [[Function]] $g: \mathbb{R} \to \mathbb{R}$ of a univariate, continuous [[Random Variable]] $X \sim p(x)$ by a [[Target Space]] $\mathcal{X}$ is given as the following

$$
\mathbb{E}_{x}[g(x)] = \int_{\mathcal{X}} g(x)p(x) \, dx
$$

## Univariate Discrete Definition

The [[Expected Value]] of a [[Function]] $g: \mathbb{R} \to \mathbb{R}$ of a univariate, discrete [[Random Variable]] $X \sim p(x)$ by a [[Target Space]] $\mathcal{X}$ is given as the following

$$
\mathbb{E}_{x}[g(x)] = \sum_{x \in \mathcal{X}} g(x)p(x)
$$

## Multivariate Definition

The [[Expected Value]] of a multivariate [[Random Variable]] $X \sim p(x)$ by a [[Target Space]] $\mathcal{X}$ is given as the following [[Matrix]]

$$
\mathbb{E}_{x}[g(x)] =
\begin{bmatrix}
\mathbb{E}_{x_{1}}[g(x_{1})] \\
\vdots \\
\mathbb{E}_{x_{D}}[g(x_{D})]
\end{bmatrix}
$$

## Linearity

Given a real-valued [[Function]] as shown in the following

$$
f(x) = ag(x) + bh(x), \;
a, b \in \mathbb{R}, x \in \mathbb{R}^D
$$

It can be shown that the [[Expected Value|Expectation]] is a linear operator

$$
\begin{align}
\mathbb{E}_{X}[f(x)]
&= \int f(x)p(x) \, dx \\
&= \int [ag(x)+bh(x)]p(x) \, dx \\
&= a \int g(x)p(x) \, dx + b \int h(x)p(x) \, dx \\
&= a \mathbb{E}_{X}[g(x)] + b\mathbb{E}_{X}[h(x)]
\end{align}
$$

## Mean of an Affine Transformation

Given a [[Random Variable]] $X$ with an [[Affine Transformation]] $y = Ax + b$, the [[Mean]] is defined as the following

$$
\mathbb{E}_{Y}[y]
= E_{X}[Ax] + b
= A E_{X}[x] + b
$$

## References

1. Mathematics for Machine Learning, pp. 187-189. 194
