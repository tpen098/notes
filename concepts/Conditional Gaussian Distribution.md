---
aliases: [Conditional Gaussian, Conditional Gaussian Distributions]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 8:46:34 pm
date modified: Sunday, August 16th 2026, 10:59:43 pm
---

# Conditional Gaussian Distribution

## Definition

The [[Conditional Gaussian Distribution]] $p(x|y)$ is a [[Gaussian Distribution]] given as the following

$$
\begin{align}
p(x|y)
&= \mathcal{N}(\mu_{x|y}, \Sigma_{x|y}) \\
\mu_{x|y}
&= \mu_{x} + \Sigma_{xy}\Sigma_{yy}^{-1}(y-\mu_{y}) \\
\Sigma_{}{x|y}
&= \Sigma_{xx} - \Sigma_{xy}\Sigma_{yy}^{-1} \Sigma_{yx}
\end{align}
$$

Where the diagonal components $\Sigma_{xx}, \Sigma_{yy}$ are marginal [[Covariance|Covariance Matrices]] for the [[Variance]] of $x$ and $y$ respectively, and $\Sigma_{xy}, \Sigma_{yx}$ are the cross-[[Covariance|Covariance Matrices]] between $x$ and $y$.

## Definition

1. Mathematics for Machine Learning, p. 199
