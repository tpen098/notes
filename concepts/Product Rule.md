---
aliases: []
tags: [statistics-probability]
date created: Sunday, August 16th 2026, 11:00:37 pm
date modified: Friday, August 21st 2026, 3:02:42 pm
---

# Product Rule

## Definition

The [[Derivative Product Rule|Product Rule]] relates the [[Joint Probability Density Function]] or [[Joint Probability Mass Function]] to the [[Conditional Probability Density Function]] or [[Conditional Probability Mass Function]] using the [[Marginal Probability Density Function]] or [[Marginal Probability Mass Function]]via following [[concepts/Expression]]:

$$
p(x, y) = p(y|x)p(x) = p(x|y)p(y)
$$

## Discrete Connection

For the discrete case, [[Probability Mass Function]], the [[Joint Probability Mass Function]] can be obtained using the [[Conditional Probability Mass Function]] if $X=x_{i}$ were known and confirming it by multiplying with the [[Marginal Probability Mass Function]] of $X$

## Continuous Connection

For the continuous case in a [[Probability Density Function]], the [[Joint Probability Density Function]] can be obtained using the [[Conditional Probability Density Function]] if $X=x_{i}$ were known and confirming it by multiplying with the [[Marginal Probability Density Function]] of $X$.

Conversely, for a continuous case in a [[Cumulative Distribution Function]], the [[Joint Cumulative Distribution Function]] can be obtained using the [[Conditional Cumulative Distribution Function]] if $X=x_{i}$ were known and confirming it by multiplying with the [[Marginal Cumulative Distribution Function]] of $X$.

## References

1. Mathematics for Machine Learning, pp. 184-185
