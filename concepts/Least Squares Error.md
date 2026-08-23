---
aliases: [L2 Loss, Least-Squares Loss, Squared Error Loss]
tags: [optimization, machine-learning]
date created: Sunday, November 13th 2022, 10:19:14 am
date modified: Friday, August 21st 2026, 10:00:34 am
---

# Least Squares Error

## Definition

The [[Loss Function]] can be defined using the [[Dot Product]]

$$
\begin{align}
f(y_{n}, \hat{y}_{n})
&= \lVert y_{n} - \hat{y}_{n} \rVert_{2} \\
&= \sum_{i=1}^{n} (y_{n, i} - \hat{y}_{n, i} )^2 \\
&= (y_{n} - \hat{y}_{n})^{\top}(y_{n} -\hat{y}_{n}) \\
\end{align}
$$

## Normalization

The [[Least Squares Error|L2 Loss]] can sometimes be factored by $\frac{1}{n}$ to normalize the [[Loss Function]] by the number of samples.

$$
\begin{align}
f(y_{n}, \hat{y}_{n})
&= \frac{1}{n}
\lVert y_{n} - \hat{y}_{n} \rVert_{2} \\
&= \frac{1}{n}
\sum_{i=1}^{n} (y_{n, i} - \hat{y}_{n, i} )^2 \\
&= \frac{1}{n}
(y_{n} - \hat{y}_{n})^{\top}(y_{n} -\hat{y}_{n}) \\
\end{align}
$$

## Square Root Application

The [[Root Function|Square Root Function]] may be applied to the entirety of the [[Least Squares Error|L2 Loss]] to normalize the magnitude of the [[Loss Function]]. The analysis is unchanged.

$$
\begin{align}
f(y_{n}, \hat{y}_{n})
&= \sqrt{ \lVert y_{n} - \hat{y}_{n} \rVert_{2} } \\
&= \sqrt{ \sum_{i=1}^{n} (y_{n, i} - \hat{y}_{n, i} )^2} \\
&= \sqrt{(y_{n}-\hat{y}_{n})^{\top}(y_{n} -\hat{y}_{n})} \\
\end{align}
$$

## References

[1]: Mathematics for Machine Learning, pp. 260-261
