---
aliases: [Univariate Change of Variable Techniques, Change of Variables, Change of Variable]
tags: [statistics-probability]
date created: Wednesday, November 9th 2022, 7:17:11 pm
date modified: Friday, August 21st 2026, 3:41:26 pm
---

# Univariate Change of Variable Technique

## Intuition Using Substitution Rule

The idea _change of variables_ comes from the idea of changing the variable of integration when faced with a difficult [[Integral]]. For univariate functions, the [[Substitution Rule]] is used

$$
\begin{align}
\int f(g(x))g'(x)\, dx &= \int f(u) \, du \\
u &= g(x) \\
du &= g'(x)dx \\
\end{align}
$$

## Cumulative Distribution Function

Consider a univariate [[Random Variable]] $X$ and an [[System Invertibility|Invertible]] [[Function]] $U$ which gives another [[Random Variable]] $Y=U(X)$. Assuming $x \in [a, b]$, the [[Cumulative Distribution Function]] is defined as the following

$$
F_{Y}(y) = P(Y \leq y)
$$

In an interest for a [[Function]] $U$ of the [[Random Variable]] $X$

$$
P(Y \leq y) = P(U(X) \leq y)
$$

Assuming $U$ is strictly increasing, applying the inverse $U^{-1}$ to the arguments of the [[Cumulative Distribution Function]] results to

$$
P(U(X) \leq y)
= P(U^{-1}(U(X)) \leq U^{-1}(y))
= P(X \leq U^{-1}(y))
$$

This can then be expressed formally using the [[Integral]] definition of the [[Cumulative Distribution Function]] as shown

$$
P(X \leq U^{-1}(y)) = \int _{a}^{U^{-1}(y)} f(x) \, dx
$$

## Probability Density Function

The [[Probability Density Function]] can be obtained by [[Derivative|Differentiation]] of the [[Cumulative Distribution Function]] from earlier, with respect to $y$

$$
f(y)
= \frac{d}{dy} F_{y}(y)
= \frac{d}{dy} \int _{a}^{U^{-1}(y)} f(x) \, dx
$$

However, this representation is in terms of $x$. Using the [[Substitution Rule]], the [[Function]] reevaluates to the following

$$
f(y) =
\frac{d}{dy}
\int_{a}^{U^{-1}(y)}
f_{x}(U^{-1}(y))U^{-1'}(y) \, dy
$$

This can be further simplified to the following form

$$
f(y) = f_{x}(U^{-1}(y)) \cdot
\left( \frac{d}{dy} U^{-1}(y) \right)
$$

If $U$ is strictly decreasing instead, then the derivate term is taken by its absolute value to retain the same expression

$$
f(y) =
f_{x}(U^{-1}(y))
\left\lvert \frac{d}{dt} U^{-1}(y) \right\rvert
$$

> [!note] Change in Unit Volume
> The [[Partial Derivative|Jacobian]] term measures the change in unit volume when applying [[Function]] $U$

## References

1. Mathematics for Machine Learning, pp. 217-219
