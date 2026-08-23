---
aliases: [Root Mean Squared Deviation, RMSE, RMDE]
tags: [optimization, machine-learning]
date created: Sunday, November 13th 2022, 10:42:46 am
date modified: Friday, August 21st 2026, 2:43:51 pm
---

# Root Mean Squared Error

## Definition

---

The [[Loss Function]] can be defined as the square root of the [[Mean]] of the [[Least Squares Error|Least-Squares Loss]] over the number of samples used, or the square root of the [[Mean Squared Error]]. [^1]

$$
f(y_{n}, \hat{y}_{n})
= \sqrt{ \frac{1}{N} \lVert y_{n} - \hat{y}_{n} \rVert_{2}^{2} }
= \sqrt{ \frac{1}{N} \sum_{i=1}^N (y_{n, i} - \hat{y}_{n, i} )^2 }

$$

## Reference

1. Mathematics for Machine Learning, p. 298
