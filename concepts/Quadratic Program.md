---
aliases: [Quadratic Programming]
tags: [optimization, machine-learning]
date created: Tuesday, November 15th 2022, 3:44:01 pm
date modified: Friday, August 21st 2026, 2:37:18 pm
---

# Quadratic Program

## Definition

---

A [[Quadratic Program]] is a special case of the [[Constrained Optimization]] wherein a quadratic, [[Convex]] [[Function]] $\dfrac{1}{2}\theta ^{\top}Q\theta+c^{\top}\theta$ is minimized, with the constraint that the [[Matrix]] $A \in \mathbb{R}^{m \times d}$ [[Matrix Multiplication|Multiplied]] by $\theta$ must be less than or greater [[Vector Space|Vector]] $b\in \mathbb{R}^m$, as shown below

$$
\begin{align}
\min_{x \in \mathbb{R}^D}
\dfrac{1}{2}\theta ^{\top}Q\theta+c^{\top}\theta, Ax \leq b
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 241
