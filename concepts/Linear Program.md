---
aliases: [Linear Programming]
tags: [optimization]
date created: Tuesday, November 15th 2022, 3:27:16 pm
date modified: Friday, August 21st 2026, 10:08:46 am
---

# Linear Program

## Definition

A [[Linear Program]] is a special case of the [[Constrained Optimization]] wherein a linear [[Function]] $c^{\top}\theta$ is minimized, with the constraint that the [[Matrix]] $A \in \mathbb{R}^{m \times d}$ [[Matrix Multiplication|Multiplied]] by $\theta$ must be less than or greater [[Vector Space|Vector]] $b\in \mathbb{R}^m$, as shown below. [^1]

$$
\min_{x \in \mathbb{R}^D} c^{\top}\theta, Ax \leq b
$$

## References

1. Mathematics for Machine Learning, p. 239
