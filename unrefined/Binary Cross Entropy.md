---
aliases: []
tags:
  - optimization
  - statistics-probability
date created: Tuesday, November 15th 2022, 1:17:26 pm
date modified: Friday, August 21st 2026, 3:46:42 pm
---

# Binary Cross Entropy

## Definition

The [[Binary Cross Entropy]] is the [[Categorical Cross Entropy]] of the ground truth and prediction $y, \hat{y}$, both in terms of the [[Random Variable]] $X$ that has a [[Bernoulli Distribution]]. It is defined as shown in the following:

$$
H(y, \hat{y}) =
-\sum_{x \in X}
y_{i}\log(\hat{y}_{i}) +(1-y_{i})\log(1-\hat{y}_{i})
$$
