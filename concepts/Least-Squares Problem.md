---
aliases: [Least-Squares Problems]
tags: [optimization, machine-learning]
date created: Sunday, November 13th 2022, 12:01:55 pm
date modified: Friday, August 21st 2026, 10:05:51 am
---

# Least-Squares Problem

## Definition

Given an [[Empirical Risk]] of a [[Machine Learning Model|Predictor]] $f(x_{n}, \theta) = \theta ^{\top} x$, and [[Independent and Identically Distributed|IID]] [[Dataset]] $\mathcal{D} = \{ (x_n, y_n) \}$, the [[Loss Function]] function can be defined using the [[Least Squares Error|L2 Loss]] to form the [[Mean Squared Error]]. Minimizing this risk or loss leads to the [[Machine Learning Model|Model]] fitting the [[Dataset]]

$$
\min_{\theta \in \mathbb{R}^D}
\frac{1}{N} \sum_{n=1}^N (y_{n} - f(x_{n}, \theta))^2
$$

Substituting the predictor output $\hat{y}_{n} = f(x_{n}, \theta) = \theta ^{\top} x_{n}$ allows the form to be expressed as the following

$$
\min_{\theta \in \mathbb{R}^D}
\frac{1}{N} \sum_{n=1}^N (y_{n} - \theta^{\top} x_{n})^2 =
\min_{\theta \in \mathbb{R}^D}
\frac{1}{N} \lVert y - X \theta \rVert_{2}^2
$$

## References

1. Mathematics for Machine Learning, pp. 260-261
