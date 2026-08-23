---
aliases: []
tags: [statistics-probability]
date created: Wednesday, November 9th 2022, 6:09:43 pm
date modified: Thursday, August 20th 2026, 6:45:49 pm
---

# Distribution Function Technique

## Algorithm

1. Establish the definition of the [[Cumulative Distribution Function]] for the [[Random Variable]] of interest $Y$ related to the initial [[Random Variable]] $X$

$$
F_{Y}(y) = P(Y \leq y)
$$

1. Apply transformation to the [[Random Variable]] of interest

$$
F_{Y}(y) = P(U(X) \leq y)
$$

1. Invert the transformation (move to right side)

$$
F_{Y}(y) = P(X \leq U^{-1}(y))
$$

1. Solve for the [[Cumulative Distribution Function]] with $f(x=t)$

$$
F_{Y}(y) = \int_{0} ^{U^{-1}(y)} f(t) \, dt
$$

1. If the [[Probability Density Function]] is needed, find the [[Derivative]] of the previous step with respect to $y$

$$
f(y) = \frac{d}{dy} F_{Y}(y)
$$

## Derivation

The Derivation of the [[Distribution Function Technique]] follows directly from the [[Univariate Change of Variable Technique]]

## Example

Consider a continuous [[Random Variable]] $X$ with [[Probability Density Function]] on $0 \leq x \leq 1$

$$
f(x) = 3 x^2
$$

To find the [[Probability Density Function]] $Y=X^2$, the steps are shown in the following

$$
\begin{align}
F_{Y}(y)
&= P(Y \leq y) \\
&= P(X^2 \leq y) \\
&= P(X \leq y^{1/2}) \\
&= \int _{0}^{y^{1/2}} 3t^2 \, dt = y^{3/2} \\
f(y)
&= \frac{d}{dy} F_{Y}(y) = \frac{3}{2}y^{1/2}
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 215-221
