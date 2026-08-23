---
aliases:
  - MAE
  - Mean Absolute Errors
tags:
  - optimization
  - machine-learning
date created: Tuesday, November 15th 2022, 11:09:05 am
date modified: Friday, August 21st 2026, 2:06:53 pm
---

# Mean Absolute Error

## Definition

The [[Loss Function]] can be defined as the [[Mean]] of the [[Least Absolute Error|L1 Loss]] by batch size $b_n$

$$

f(y_{n}, \hat{y}_{n}) =
\frac{1}{b_{n}}
\sum_{b=1}^{b_{n}}
\lVert y_{n} - \hat{y}_{n} \rVert_{1}
$$
