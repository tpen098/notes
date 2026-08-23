---
aliases: [Model, Predictor, Machine Learning Models, Models, Predictors]
tags: [machine-learning]
date created: Sunday, November 13th 2022, 10:57:45 am
date modified: Friday, August 21st 2026, 10:20:49 am
---

# Machine Learning Model

## Definition as a Linear Function Predictor

A [[Machine Learning Model]] can be thought of as a [[Function]] that, given a particular [[Model Input]], produces a prediction. Assuming a [[Linear Mapping]], the [[Function]] applies a scaling factor $\theta$ to the input and adds a bias $\theta_{0}$

$$
\begin{align}
f(x, \theta) &= \theta_{0} + \theta ^{\top} x \\
f(x, \theta) &= \theta_{0} + \sum_{d=1}^{D} \theta_{d} x_{n}^{(d)} \\
\end{align}
$$

## Definition as a Probabilistic Predictor

Given that [[Model Input|Model Inputs]] may be noisy, there is a need to quantify the effect of the noise and express a level of confidence or certainty on the output, or prediction. A [[Machine Learning Model]] [[Function]] can then be thought of as a [[Probability|Probability Distribution]].

## References

1. Mathematics for Machine Learning, pp. 254-256, 259
