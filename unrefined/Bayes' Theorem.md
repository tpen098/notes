---
aliases:
  - Bayes' Law
  - Bayes' Rule
  - Bayesian Mechanics
tags:
  - statistics-probability
date created: Wednesday, November 2nd 2022, 1:29:14 pm
date modified: Thursday, August 20th 2026, 6:16:08 pm
---

# Bayes' Theorem

## Derivation from Product Rule

Using [[concepts/Sum Rule|Marginalization]], [[Bayes' Theorem]] can be derived as follows

$$
\begin{align}
p(x, y) &= p(x|y)p(y) \\
p(x, y) &= p(y|x)p(x) \\
p(x|y)p(y) &= p(y|x)p(x) \\
\end{align}
$$

## Definition

From the prior derivation, [[Bayes' Theorem]] takes the forms below

$$
\begin{align}
p(x|y) = \frac{p(y|x)p(x)}{p(y)} \\
p(y|x) = \frac{p(x|y)p(y)}{p(x)} \\
\end{align}
$$

## Interpretation

With a subjective, prior knowledge of $\omega$ via $p(\omega)$, a likelihood $p(\theta | \omega)$ that relates $\theta$ and $\omega$, under the _evidence_ $p(\theta)$, a conclusion can be made for $\omega$ given knowledge on $\theta$.

## Reference

1. Mathematics for Machine Learning, p. 185
