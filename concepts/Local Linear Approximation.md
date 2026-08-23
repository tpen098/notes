---
aliases: [Local Linear Approximations]
tags: [optimization]
date created: Monday, October 24th 2022, 7:01:26 pm
date modified: Friday, August 21st 2026, 10:16:30 am
---

# Local Linear Approximation

## Definition

The [[Local Linear Approximation]] of a [[Function]] $f$ is an approximation of the function around point $f(x_0)$

$$
f(x) \approx f(x_{0}) + ((\nabla_{x}f)(x_{0}))(x-x_{0})
$$

> [!note] Accuracy of the Approximation
> The further away $x$ is from $x_0$, the worse the approximation becomes.

## References

1. Mathematics for Machine Learning, pp. 165-166
