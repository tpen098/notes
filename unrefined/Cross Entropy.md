---
aliases:
  - Cross Entropies
tags:
  - optimization
  - statistics-probability
date created: Sunday, November 13th 2022, 9:42:15 pm
date modified: Friday, August 21st 2026, 3:45:48 pm
---

# Cross Entropy

## Definition

The [[Cross Entropy]] of the [[Model Label|Ground Truth]] and prediction $y, \hat{y}$, both in terms of the continuous [[Random Variable]] $X$, is defined as their [[Inner Product]] or the [[Integral]] of the truth and the [[Logarithm]] of the prediction with respect to $X$.

$$
\begin{align}
H(y, \hat{y})
&= \langle y, -\log(\hat{y}) \rangle \\
&= - \int_{a}^{b} y \log(\hat{y}) \, dx
\end{align}
$$
