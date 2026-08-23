---
tags:
  - statistics-probability
aliases:
  - Conjugate
  - Conjugacy
date created: Tuesday, November 8th 2022, 3:11:16 pm
date modified: Sunday, August 16th 2026, 11:02:43 pm
---

# Conjugate Prior

## Definition

Considering [[Bayes' Theorem]]. The _posterior_ is the component $p(x|y)$, the _likelihood_ is the component $p(x|y)$, the _prior_ is the component $p(y)$, and the component $p(x)$ is the evidence

$$
p(y|x) = \dfrac{p(x|y)p(y)}{p(x)}
$$

> [!Note]
> The evidence is a normalizing factor for the posterior.

A _prior_ is a [[Conjugate Prior|Conjugate]] for the _likelihood_ if it has the same form or type as the _posterior_. This [[Conjugate Prior|Conjugacy]] makes calculation of the product $p(x|y)p(y)$ algebraically convenient.

## Summary Table

| Likelihood                 | Conjugate Prior           | Posterior                 |
| -------------------------- | ------------------------- | ------------------------- |
| [[Bernoulli Distribution]] | [[Beta Distribution]]     | [[Beta Distribution]]     |
| [[Binomial Distribution]]  | [[Beta Distribution]]     | [[Beta Distribution]]     |
| [[Gaussian Distribution]]  | [[Gaussian Distribution]] | [[Gaussian Distribution]] |

## References

1. Mathematics for Machine Learning, pp. 208-210
