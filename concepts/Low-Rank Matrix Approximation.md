---
aliases: [Low-Rank Matrix Approximations]
tags: [linear-algebra]
date created: Thursday, October 20th 2022, 11:41:33 am
date modified: Friday, August 21st 2026, 10:18:25 am
---

# Low-Rank Matrix Approximation

## Definition

Consider a [[Singular Value Decomposition]] of a [[Matrix]] $A$ wherein _singular values_ in the [[Singular Value Matrix]] are in descending order.

The [[Rank]] $k$ approximation of $A$ is defined as the following

$$
A \approx \hat{A}(k)=\sum_{i=1}^k \sigma_i u_i v_i^{\top}
$$

## Element Count

For a [[Matrix]] with dimensions $x \times y$, a rank $k$ approximations allows the following number of elements.

$$
m \times n \geq k(m+n+1)
$$

## References

1. Mathematics for Machine Learning, Ch.4, pp. 129-131
