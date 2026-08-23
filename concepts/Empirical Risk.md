---
aliases: [Empirical Risks]
tags: [machine-learning]
date created: Sunday, November 13th 2022, 11:49:16 am
date modified: Thursday, August 20th 2026, 6:27:50 pm
---

# Empirical Risk

## Definition

The [[Empirical Risk]] is defined as the [[Empirical Mean]] of a given [[Loss Function]], an [[Independent and Identically Distributed|IID Dataset]] $(X, y)$ and [[Machine Learning Model|Predictor]] $f$ with its prediction $\hat{y}_{n} = f(x_{n}, \theta)$.

$$
R_{emp}(f, X, y) = \frac{1}{N} \sum_{n=1}^N l(y_{n}, \hat{y}_{n})
$$

## References

1. Mathematics for Machine Learning, pp. 259-260
