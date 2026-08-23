---
aliases: [Linear Program Lagrangian]
tags: [optimization]
date created: Tuesday, November 15th 2022, 3:36:39 pm
date modified: Friday, August 21st 2026, 10:09:06 am
---

# Linear Program Lagrangian Duality

## Derivation

The [[Constrained Optimization|Lagrangian]] of a [[Linear Program]] is given as the following

$$
\begin{align}
\mathfrak{L}(\theta, \lambda)
&= c^{\top}\theta + \lambda ^{\top}(A\theta-b) \\
&= (c + A^{\top} \lambda)^{\top}\theta - \lambda ^{\top}b
\end{align}
$$

If the [[Derivative]] of both sides were taken with respect to $\theta$ for minimization, then the equation takes the following form

$$
c+A^{\top}\lambda = 0
$$

## Definition

This results to the [[Lagrangian Duality]] taking the following form.

$$
\begin{align}
\max_{\lambda \in \mathbb{R}^m}
-\lambda ^{\top} b \\
c + A^{\top}\lambda
= 0, \lambda \geq 0
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 239-240
