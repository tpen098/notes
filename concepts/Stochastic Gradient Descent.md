---
aliases: [SGD]
tags: [optimization, machine-learning]
date created: Tuesday, November 15th 2022, 1:49:56 pm
date modified: Friday, August 21st 2026, 3:16:51 pm
---

# Stochastic Gradient Descent

## Definition

In standard [[Gradient Descent]], the entire [[Dataset]] is used to estimate the [[Partial Derivative|Gradient]] of a [[Function]] to determine its minimum. If the [[Dataset]] is too large, the [[Gradient Descent]] can opt to use random samples of the [[Dataset]], _mini-batch_, for an approximation of the [[Partial Derivative|Gradient]] instead. [^1]

$$
\begin{align}
f(\theta) &
= \sum_{n=1}^{N} f_{n}(\theta) \\
\theta_{i+1} &
= \theta_{i}
- \epsilon_{i}
  \sum_{n=1}^{n_{s}} ((\nabla f_{n}) (\theta_{i}))
^ {\top}
, n_{s} \leq N \\
\end{align}
$$

## References

[^1]: Mathematics for Machine Learning, pp. 231-233
