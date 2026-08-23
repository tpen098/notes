---
aliases: [Conditional PMF]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 1:06:57 pm
date modified: Friday, August 21st 2026, 3:45:24 pm
---

# Conditional Probability Mass Function

## Definition

Given [[Random Variable|Random Variables]] $X, Y$, the _Conditional [[Probability Mass Function]]_ $p(x|y)$ is defined as the [[Probability]] of $X=x_i$ given that $Y=y_j$ is guaranteed.

From the [[concepts/Product Rule|Product Rule]], the [[Conditional Probability Mass Function]] can be defined using the [[Joint Probability Mass Function]] and [[Marginal Probability Mass Function]] as shown

$$
p(x|y) = \frac{p(x, y)}{p(y)}
$$

## Two-Dimensional Example

Given [[Random Variable|Random Variables]] $X, Y$, the [[Conditional Probability Mass Function]] $p(x_{i}|y_{j})$ is defined as the intersection between $x_i$ and $y_j$ over the sum of all possible [[Probability|Probabilities]] with $x_i$ under the column $y_j$.

$$
\begin{matrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{m} \\
\end{matrix}
\begin{array}{| c | }
\hline
p_{1j} \\
\hline
p_{2j} \\
\hline
\vdots \\
\hline
p_{mj} \\
\hline
\end{array}
\atop
y_{j}
$$

> [!note] Non-Intersecting
> The numerator in a [[Conditional Probability Mass Function]] can be zero if $x_i$ and $y_j$ has no intersection.

## References

1. Mathematics for Machine Learning, pp. 179-180, 184-185
2. Introduction to mathematical statistics, p. 94
