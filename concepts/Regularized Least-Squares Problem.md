---
aliases: [Regularized Least-Squares Problems]
tags: [optimization, machine-learning]
date created: Sunday, November 13th 2022, 12:13:14 pm
date modified: Friday, August 21st 2026, 2:43:23 pm
---

# Regularized Least-Squares Problem

## Statement

[[Regularization]] can be applied to the [[Least-Squares Problem]] by adding a [[Regularization|Penalty Term]] as shown in the following

$$
\min_{\theta \in \mathbb{R}^D}
\frac{1}{N} \lVert y - X \theta \rVert_{2}^2
\boxed{+\lambda \lVert \theta \rVert_{2}^{2}}
$$

This penalizes large parameter values which often increase during overfitting

## References

1. Mathematics for Machine Learning, pp. 262-263
