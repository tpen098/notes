---
aliases: [PMF, Discrete Probability, Probability Mass Functions, Discrete Probabilities]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 12:18:34 pm
date modified: Sunday, August 23rd 2026, 11:54:47 am
---

# Probability Mass Function

## Definition

Given a discrete [[Target Space]], the [[Probability Mass Function]] is a [[Function]] $f: \mathbb{R}^D \to \mathbb{R}$ that defines the [[Probability]] $f(x_{i}) = P(X =x_{i})$ that a [[Random Variable]] $X$ will take a particular value $x \in \mathcal{T}$.

## Properties

All outputs of the [[Probability Mass Function]] is within the range $[0, 1]$ and the sum of all possible outputs equal exactly $1$.

$$
\begin{align}
\forall x_{i} \in \mathcal{T}&: 0 \leq f(x_i) \leq 1 \\
\forall x_{i} \in \mathcal{T}&: \sum_{i=1}^{n} f(x_{i}) = 1 \\

\end{align}
$$

## References

1. Mathematics for Machine Learning, p. 178
2. Applied Statistics and Probability for Engineers, p. 46
