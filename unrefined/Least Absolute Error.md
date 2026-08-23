---
aliases:
  - L1 Loss
  - Least Absolute Deviations
  - Least Absolute Residuals
  - Least Absolute Values
  - LAD
  - LAE
  - LAR
  - LAV
tags:
  - optimization
  - machine-learning
date created: Sunday, November 13th 2022, 10:16:27 am
date modified: Friday, August 21st 2026, 9:59:33 am
---

# Least Absolute Error

## Definition

The [[Loss Function]] can be defined using the [[Manhattan Norm]]

$$
\begin{align}
f(y_{n}, \hat{y}_{n})
&= \lVert y_{n} - \hat{y}_{n} \rVert_{1} \\
&= \sum_{i=1}^n \lvert \hat{y}_{n, i} - y_{i} \rvert
\end{align}
$$

## Normalization

The [[Least Absolute Error|L1 Loss]] can sometimes be factored by $\frac{1}{n}$ to normalize the [[Loss Function]] by the number of samples.

$$
\begin{align}
f(y_{n}, \hat{y}_{n})
&= \frac{1}{n}
\lVert y_{n} - \hat{y}_{n} \rVert_{1} \\
&= \frac{1}{n}
\sum_{i=1}^n \lvert \hat{y}_{n, i} - y_{i} \rvert
\end{align}
$$

## References
