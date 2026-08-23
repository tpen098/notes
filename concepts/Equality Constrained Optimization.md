---
aliases: [Equality Constrained Optimizations]
tags: [optimization]
date created: Tuesday, November 15th 2022, 2:28:26 pm
date modified: Friday, August 21st 2026, 3:46:46 pm
---

# Equality Constrained Optimization

## Definition

Given a real-valued [[Function]] $f: \mathbb{R}^D \to \mathbb{R}$, [[Equality Constrained Optimization]] is defined as the minimization of the [[Function]] $f$ with respect to its arguments $\theta$ while satisfying the condition $g_{i}(\theta) \leq 0, \forall i$ and $h_{j}(\theta) = 0, \forall j$

$$
\min_{\theta} f(\theta)
, g_{i}(\theta) \leq 0,\forall i
, h_{j}(\theta) = 0, \forall j
$$

## References

1. Mathematics for Machine Learning, pp. 235-236
