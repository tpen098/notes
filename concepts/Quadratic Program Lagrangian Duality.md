---
aliases: [Quadratic Program Lagrangian]
tags: [optimization]
date created: Tuesday, November 15th 2022, 3:36:39 pm
date modified: Friday, August 21st 2026, 2:37:51 pm
---

# Quadratic Program Lagrangian Duality

## Derivation

The [[Constrained Optimization|Lagrangian]] of a [[Quadratic Program]] is given as the following

$$
\begin{align}
\mathfrak{L}(\theta, \lambda) &
= \dfrac{1}{2} \theta ^{\top} Q \theta
+ c^{\top}\theta
+ \lambda(Ax-b) \\
&
= \dfrac{1}{2} \theta ^{\top} Q \theta
+ (c+A^{\top}\lambda)^{\top}\theta
- \lambda ^{\top}b \\
\end{align}
$$

If the [[Derivative]] of both sides were taken with respect to $\theta$ for minimization, then the equation takes the following form

$$
Q\theta + (c+A^{\top}\lambda) = 0
$$

Assuming $Q$ is [[Matrix Inverse|Invertible]], the form changes to the following

$$
\theta = 0Q^{-1}(c+A^{\top}\lambda)
$$

## Definition

Substituting the value of $\theta$ into the [[Constrained Optimization|Lagrangian]], the [[Lagrangian Duality]] takes the following form

$$
\begin{align}
\max_{\lambda \in \mathbb{R}^m}
-\frac{1}{2}
(c+A^{\top}\lambda)^{\top}
Q^{-1}(c+A^{\top}\lambda)
- \lambda ^{\top}b
,\lambda \geq 0
\end{align}
$$

## References

1. [[@Mathematics for Machine Learning]] (pp. 241-242)
