---
aliases: [Joint CDF, Joint Cumulative Distribution Functions]
tags: [statistics-probability]
date created: Wednesday, November 2nd 2022, 9:13:24 am
date modified: Friday, August 21st 2026, 9:55:18 am
---

# Joint Cumulative Distribution Function

## Definition

Given [[Random Variable|Random Variables]] $X = \{ X_{1}, \dots, X_{n} \} \in \mathbb{R}^D$, of a continuous [[Target Space]], the _Joint [[Cumulative Distribution Function]]_ of $X$ with states $x_{i} \in \mathcal{T}_{i}$ is defined as the following [^1][^2][^3]

$$
\begin{align}
F_{X}(x)
&= P(X_{1} \leq x_{1}, \dots, X_{D} \leq x_{d}) \\
&= \int_{-\infty}^{x_{n}} \dots \int_{-\infty}^{x_{1}}
f(x_{1}, \dots, x_{D}) \; dx_1 \dots dx_D
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 181-182
2. Applied Statistics and Probability for Engineers, p. 98
3. Introduction to mathematical statistics, p. 74
