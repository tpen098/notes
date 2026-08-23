---
aliases: [Taylor Polynomials]
tags: [calculus]
date created: Thursday, October 20th 2022, 5:14:40 pm
date modified: Friday, August 21st 2026, 3:35:48 pm
---

# Taylor Polynomial

## Definition

The [[Taylor Polynomial]] of degree $n$ of [[Function]] $f: \mathbb{R} \to \mathbb{R}$ at $x_0$ is defined as the following

$$
T_n(x) := \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!}(x-x_{0})^k
$$

Where $f^{(k)}(x_{0})$ is the $k$th [[Derivative]] of $f$ at $x_0$ (assuming it exists)

> [!NOTE] Function Representation
> The [[Taylor Polynomial]] of degree $n$ is an approximation of a [[Function]] which does not need to be a polynomial.

## References

1. Mathematics for Machine Learning, Ch. 5, p. 142
