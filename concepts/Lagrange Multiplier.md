---
aliases: [Lagrange Multipliers, Dual Variable, Dual Variables]
tags: [optimization]
date created: Tuesday, November 15th 2022, 2:14:24 pm
date modified: Friday, August 21st 2026, 9:58:51 am
---

# Lagrange Multiplier

## Definition

---

Given a [[Constrained Optimization|Langrarian]] problem, the constraint $g_{i}(x) \leq 0, \forall i$ can be embedded into the base [[Function]] $f$ linearly by scaling each constraint with a multiplier $\lambda \geq 0$, known as the [[Lagrange Multiplier|Lagrange Multipliers]]. [^1]

$$
\begin{align}
\mathfrak{L}(\theta, \lambda)
&= f(\theta)
+ \sum_{i=1}^{m}\lambda_{i} g_{i}(x) \\
&= f(\theta) + \lambda ^{\top} g(\theta) \\
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 233-234)
