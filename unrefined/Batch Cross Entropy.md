---
aliases:
  - Mean Cross Entropy
  - Batch Cross Entropies
tags:
  - optimization
  - statistics-probability
date created: Tuesday, November 15th 2022, 1:14:08 pm
date modified: Friday, August 21st 2026, 3:47:52 pm
---

# Batch Cross Entropy

## Definition

The [[Batch Cross Entropy]] is the [[Empirical Mean]] of the [[Cross Entropy]], [[Categorical Cross Entropy]], or [[Binary Cross Entropy]]. It is defined as the following:

$$
H_{b}(y, \hat{y}) =
\frac{1}{b_{n}}
\sum_{b=1}^{b_{n}}
H(y_{b}, \hat{y}_{b})
$$
