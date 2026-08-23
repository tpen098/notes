---
aliases:
  - Joint PDF
tags:
  - statistics-probability
date created: Wednesday, November 2nd 2022, 9:26:28 am
date modified: Friday, August 21st 2026, 9:56:31 am
---

# Joint Probability Density Function

## Definition

---

Given [[Random Variable|Random Variables]] $X = \{ X_{1}, \dots, X_{n} \} \in \mathbb{R}^D$, of a continuous [[Target Space]], the _Joint [[Probability Density Function]]_ is the [[Probability]] of $X$ having states $x_{i} \in \mathcal{T}_{i}$ within corresponding ranges $[a_{i}, b_{i}]$ as defined in the following: [^1][^2]

$$
P(a \leq X \leq b)
= \int_{a_n}^{b_n} \dots \int_{a_1}^{b_1}
f(x_{1}, \dots, x_{D}) \; dx_1 \dots dx_D
$$

## References

[1]: Mathematics for Machine Learning, pp. 181-182
[2]: Applied Statistics and Probability for Engineers, p. 98
