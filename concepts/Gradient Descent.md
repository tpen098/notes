---
aliases: []
tags:
  - machine-learning
date created: Tuesday, November 15th 2022, 1:30:30 pm
date modified: Friday, August 21st 2026, 9:42:18 am
---

# Gradient Descent

## Definition

[[Gradient Descent]] is a first-order, Optimization [[Algorithm]] wherein the minimum of a real-valued [[Function]] $f: \mathbb{R}^d \to \mathbb{R}$ is obtained by taking steps $e$ proportional to the negative of the [[Partial Derivative|Gradient]] of the [[Function]] at the current point.

$$
\theta_{i+1}
= \theta_{i}
- \epsilon_{i} ((\nabla f)(\theta_{i}))^{\top}
$$

## Effect of the Learning Rate

For a suitable _step size_ or _learning rate_ $\epsilon$,, commonly $\epsilon \in [1\mu, 1]$, the sequence $f(\theta_{0}) \geq f(\theta_{1}) \geq \dots$ converges to a local minimum

If the step size is too small, the [[Gradient Descent]] can be slow but if the step size is too big then the [[Gradient Descent]] can overshoot, fail to converge, or may even diverge.

## References

1. Mathematics for Machine Learning, pp. 227-230
