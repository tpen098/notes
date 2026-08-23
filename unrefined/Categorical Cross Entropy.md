---
aliases:
  - Discrete Cross Entropy
tags:
  - machine-learning
  - optimization
date created: Sunday, November 13th 2022, 9:42:15 pm
date modified: Friday, August 21st 2026, 3:45:15 pm
---


# Categorical Cross Entropy

## Definition

The [[Categorical Cross Entropy|Discrete Cross Entropy]] or [[Categorical Cross Entropy]] of the [[Model Label|Ground Truth]] and prediction $y, \hat{y}$, both in terms of the discrete [[Random Variable]] $X$, is defined as the [[Mean]] with respect to $P$ of the [[Entropy|Entropies]] of $Q$, or the [[Entropy]] of $P$ minus the [[Kullback–Leibler Divergence|Relative Entropy]] between $P, Q$.

$$
\begin{align}
H(y, \hat{y})
&= H(y) + D_{KL}(y \mid\mid \hat{y}) \\
&= -\sum_{x \in X} y \log(\hat{y}) \\
\end{align}
$$
