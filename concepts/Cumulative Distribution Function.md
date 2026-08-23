---
aliases: [CDF]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 1:40:26 pm
date modified: Sunday, August 16th 2026, 11:25:03 pm
---

# Cumulative Distribution Function

## Definition

Given a [[Random Variable]] $X$ of a continuous [[Target Space]], the [[Cumulative Distribution Function]] of $X \in \mathbb{R}$ with state $x \in \mathcal{T}$ is defined as the following

$$
\begin{align}
F_{X}(x_i)
&= P(X \leq x) \\
&= \int_{-\infty}^{x}
f(x) \; dx
\end{align}
$$

## Definition Using the Probability Density Function

Alternatively, the [[Cumulative Distribution Function]] can be thought of as a [[Probability Density Function]] with ranges $(-\infty, x]$.

$$
\begin{align}
F_{X}(x_i)
&= P(X \leq x) \\
&= P(-\infty \leq X \leq x) \\
\end{align}
$$

> [!warning] Interchangeability
> Both are often used interchangeably in references.

## References

1. Mathematics for Machine Learning, pp. 181-182
2. Applied Statistics and Probability for Engineers, p. 98
3. Introduction to mathematical statistics, p. 74
