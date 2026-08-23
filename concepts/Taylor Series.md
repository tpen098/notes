---
aliases: []
tags: [calculus]
date created: Thursday, October 20th 2022, 5:09:49 pm
date modified: Friday, August 21st 2026, 3:38:33 pm
---

# Taylor Series

## Definition

The [[Taylor Series]] is a representation of a univariate [[Function]] $f$ as an infinite sum of terms, determined using [[Derivative|Derivatives]] of $f$ evaluated at point $x_0$. [^1]

For a [[Smooth]] [[Function]] $f: \mathbb{R} \to \mathbb{R}$, the [[Taylor Series]] of $f$ at $x_0$ is defined as the following special case of a [[Power Series]]. [^1]

$$
T_{{\infty}}(x) := \sum_{k=0}^{\infty}\frac{f^{(k)}(x_{0})}{k!}(x-x_{0})^k
$$

> [!NOTE] Similarity with the Taylor Polynomial
> The [[Taylor Series]] has the same form as the [[Taylor Polynomial]] except it spans from $0$ to $\infty$ instead of up to only $n$.

## References

[^1]: Mathematics for Machine Learning, Ch. 5, pp. 142-143
