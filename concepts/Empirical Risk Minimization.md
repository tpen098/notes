---
aliases: [Empirical Risk Minimizations]
tags: [machine-learning]
date created: Sunday, November 13th 2022, 10:00:24 am
date modified: Thursday, August 20th 2026, 6:28:15 pm
---

# Empirical Risk Minimization

## Statement

Given a [[Dataset]] with $N$ pairs, the goal is to find parameter values $\theta^*$ to the [[Machine Learning Model|Predictor]] $f(\cdot, \theta): \mathbb{R}^D \to \mathbb{R}$ such that the prediction $\hat{y}_{n}$ or output of the [[Machine Learning Model|Predictor]] is close the the [[Model Label|Ground Truths]]

$$
f(x_{n}, \theta^*) = \hat{y}_{n} \approx y_{n}, \forall n
$$

Minimizing the [[Empirical Risk]] $R_{emp}$ of the [[Machine Learning Model|Predictor]] by a given [[Dataset]] requires finding the right parameters $\theta^*$.

## References

1. Mathematics for Machine Learning, pp. 259-260
