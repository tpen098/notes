---
aliases: []
tags: [mathematics, calculus]
date created: Thursday, October 20th 2022, 6:36:30 pm
date modified: Thursday, August 20th 2026, 6:34:59 pm
---

# Chain Rule

## Definition

The [[Partial Derivative]] of the product of two differentiable [[Function|Functions]] is defined as the following.

$$
\frac{ \partial g(f(x)) }{ \partial x }
= \frac{ \partial g(f(x)) }{ \partial f(x) }
  \frac{ \partial f(x) }{ \partial x }
$$

> [!NOTE] Function with Singular Output
> For a univariate [[Function]], the [[Derivative]] simplifies to the following
>
> $$
> \frac{ d g(f(x)) }{ dx }
> = \frac{ d g(f(x)) }{ d f(x) }
>   \frac{ d f(x) }{ dx }
> = \frac{ d g(f(x)) }{ d x }
>   \frac{ d f(x) }{ dx }$$

## References

1. Mathematics for Machine Learning, ch. 5, pp. 143-145
