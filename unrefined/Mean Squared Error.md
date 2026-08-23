---
aliases:
  - Mean Squared Loss
  - Mean Squared Deviation
  - MSE
  - MDE
tags:
  - optimization
  - machine-learning
date created: Sunday, November 13th 2022, 10:42:46 am
date modified: Friday, August 21st 2026, 2:07:16 pm
---

# Mean Squared Error

## Definition

The [[Loss Function]] can be defined as the [[Mean]] of the [[Least Squares Error|L2 Loss]] by batch size $b_n$

$$

f(y_{n}, \hat{y}_{n}) =
\frac{1}{b_{n}}
\sum_{b=1}^{b_{n}}
\lVert y_{n} - \hat{y}_{n} \rVert_{2}^{2}
$$
