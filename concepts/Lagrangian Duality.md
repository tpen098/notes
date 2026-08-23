---
aliases: [Lagrangian Dual Problem]
tags: [optimization]
date created: Tuesday, November 15th 2022, 2:24:00 pm
date modified: Friday, August 21st 2026, 9:59:07 am
---

# Lagrangian Duality

## Definition

Given a [[Constrained Optimization]] or [[Constrained Optimization|Primal Problem]], with _primal variables_ $\theta$. the [[Lagrangian Duality|Lagrangian Dual Problem]] is given as the following

$$
\max_{\lambda\in \mathbb{R}^m} \mathfrak{D}(\lambda),
\lambda \geq 0
$$

Where $\lambda$ are the [[Lagrange Multiplier|Dual Variables]] and the following holds

$$
\mathfrak{D}(\lambda)
= \min_{x \in \mathbb{R}^D} \mathfrak{L}(\theta, \lambda)
$$

## References

1. Mathematics for Machine Learning, p. 234
