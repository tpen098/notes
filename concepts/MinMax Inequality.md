---
aliases: [MinMax Inequalities, MinMax]
tags: [optimization]
date created: Tuesday, November 15th 2022, 2:30:48 pm
date modified: Friday, August 21st 2026, 2:09:24 pm
---

# MinMax Inequality

## Statement

For any [[Function]] $f$ with two arguments $x, y$, the maximum of the minimum of the [[Function]] is less than or equal to the minimum of its maximum.

$$
\max_{y}\min_{x} f(x, y) \leq \min_{x}\max_{y} f(x, y)
$$

This intuition is derived from the following inequality

$$
\forall x, y,
\min_{x} f(x, y) \leq \max_{y}f (x, y)
$$

## References

1. Mathematics for Machine Learning, pp. 234-235
