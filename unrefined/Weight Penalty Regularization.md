---
aliases: []
tags: [optimization, machine-learning]
date created: Sunday, November 13th 2022, 12:20:47 pm
date modified: Sunday, August 23rd 2026, 12:05:40 pm
---

# Weight Penalty Regularization

## Definition

Given a [[Empirical Risk]] with [[Loss Function]] as [[Least Squares Error|L2 Loss]] to utilize the [[Mean Squared Error]] definition for a [[Machine Learning Model|Predictor]] $f$, the weight penalty adds the scaled [[Dot Product]] of the parameter vector with itself to discourage certain values.

$$
R_{emp}(f, X, y) =
\frac{1}{N}
\sum_{n=1}^{N}(y_{n} - \hat{y}_{n})^2
+ \boxed{\lambda \theta ^{\top} \theta}
$$
