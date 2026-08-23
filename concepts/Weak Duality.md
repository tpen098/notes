---
aliases: []
tags:
  - optimization
date created: Tuesday, November 15th 2022, 2:36:34 pm
date modified: Thursday, August 20th 2026, 4:04:56 pm
---

# Weak Duality

## Statement

The _primal values_ in a [[Constrained Optimization]] problem are always greater than or equal to the _duality values_ in a [[Lagrangian Duality]] using the [[MinMax Inequality]]

$$
\min_{\theta \in \mathbb{R}^D}
\max_{\lambda \geq 0}
\mathfrak{L}(\theta, \lambda)
\geq
\max_{\lambda \geq 0}
\min_{\theta \in \mathbb{R}^D}
\mathfrak{L}(\theta, \lambda)
$$

## References

1. Mathematics for Machine Learning, p. 235
