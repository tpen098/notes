---
aliases: [Marginal Probability, Discrete Marginal Probability, Marginal PMF]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 1:00:06 pm
date modified: Friday, August 21st 2026, 10:24:12 am
---

# Marginal Probability Mass Function

## Definition

Given [[Random Variable|Random Variables]] $X_{1}, X_{2}, \dots, X_{n}$ of a discrete [[Target Space]], the _Marginal [[Probability Mass Function]]_ of $X_i$ is defined as the [[Probability]] of $X_{i}=x_{i}$ irrespective of the other [[Random Variable|Random Variables]]

$$
p(x_{i}) = P(X_{i}=x_{i})
$$

## Two-Dimensional Example

Given [[Random Variable|Random Variables]] $X, Y$, the [[Marginal Probability Mass Function]] $P(X=x_{i})$ is given as the sum of the entire column of $x_i$ if the following array were used to represent the probabilities

$$
P(X=x_{i}) = \frac{\sum_{{i=1}}^n n_{(i,j)}}{\sum n}
$$

$$
\begin{matrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{m} \\
\end{matrix}
\begin{array}{| c | c | c | }
\hline
n_{11} & n_{12} & \dots & n_{1n}\\
\hline
n_{21} & n_{22} & \dots & n_{2n} \\
\hline
\vdots & \vdots & \ddots & \vdots \\
\hline
n_{m_{1}} & n_{m_{2}} & \dots & n_{mn} \\
\hline
\end{array}
\atop
\begin{matrix}
y_{1} & y_{2} & \;\;\;\; \dots & y_{n} \\
\end{matrix}
$$

## References

1. Mathematics for Machine Learning, pp. 177-178
