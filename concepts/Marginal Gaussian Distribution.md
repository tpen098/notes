---
aliases: [Marginal Gaussian, Marginal Gaussian Distributions]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 9:01:15 pm
date modified: Friday, August 21st 2026, 10:23:20 am
---

# Marginal Gaussian Distribution

## Definition

Given a [[Joint Gaussian Distribution]] of two [[Random Variable|Random Variables]] $X, Y$, the [[Marginal Gaussian Distribution]] can be computed by applying the [[concepts/Sum Rule]] as shown in the following

$$
\begin{align}
p(x) &
= \int p(x, y) \, dy
= \mathcal{N}(x|\mu_{x}, \Sigma_{xx})
\\
p(y) &
= \int p(x, y) \, dx
= \mathcal{N}(x|\mu_{y}, \Sigma_{yy})
\end{align}
$$

## Definition

1. Mathematics for Machine Learning, pp. 199-200
