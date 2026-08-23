---
aliases: [PDF, Probability Density Functions]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 1:40:26 pm
date modified: Friday, August 21st 2026, 2:31:25 pm
---

# Probability Density Function

## Definition

Given a continuous [[Target Space]], the [[Probability Density Function]] is the [[Function]] $f: \mathbb{R}^D \to \mathbb{R}$ that defines the [[Probability]] that a [[Random Variable]] $X$ will take a value $x \in \mathcal{T}$ within the range $[a, b]$.

$$
P(a \leq X \leq b)
= \int_{a}^{b} f(x) \; dx
$$

## Properties

All outputs of the [[Probability Density Function]] are non-negative and the integral of all possible outputs equal exactly $1$.

$$
\begin{align}
\forall x \in \mathbb{R}^D: f(x) \geq 0 \\
\int _{\mathbb{R}^D} f(x) \, dx = 1 \\
\end{align}
$$

> [!NOTE] Probability Density Function at a Point
> The value for a point is zero because the [[Integral]] ends are equal $a=b$

## References

1. Mathematics for Machine Learning, pp. 181-182
2. Applied Statistics and Probability for Engineer, p. 98
