---
aliases: [Statistically Independent, Independent]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 6:22:12 pm
date modified: Friday, August 21st 2026, 3:16:14 pm
---

# Statistical Independence

## Definition

Two [[Random Variable|Random Variables]] $X, Y$ are [[Statistical Independence|Statistically Independent]] if the value of $y$ doesn't add any additional information about $x$ or vice versa. Alternatively, the [[Conditional Probability Density Function|Conditional PDF]], [[Conditional Cumulative Distribution Function|Conditional CDF]], or [[Conditional Probability Mass Function|Conditional PMF]] only yields the [[Marginal Probability Density Function|Marginal PDF]], [[Marginal Cumulative Distribution Function|Marginal CDF]], or [[Marginal Probability Mass Function|Marginal PMF]] respectively as shown.

$$
p(y|x) = p(x)
\atop
p(x|y) = p(y)
$$

Mathematically, this is if and only if the following holds

$$
p(x, y) = p(x)p(y)
$$

## Covariance

The [[Covariance]] of the two [[Random Variable|Random Variables]] is zero as a result.

$$
Cov_{X, Y}[x, y] = Cov_{Y, X}[y, x] = 0
$$

> [!warning] The Converse doesn't hold
> Two [[Random Variable|Random Variables]] can have zero [[Covariance]] but not be [[Statistical Independence|Statistically Independent]].

## Variance

The [[Variance]] of the sums of the [[Random Variable|Random Variables]] is simply the sum of the [[Variance]] of $X$ and the [[Variance]] of $Y$ as the [[Covariance|Covariances]] are zero

$$
\mathbb{V}_{X, Y}[x, y]
= \mathbb{V}_{Y, X}[y, x]
= \mathbb{V}_{X}[x] + \mathbb{V}_{Y}[y]
$$

## References

[1]: Mathematics for Machine Learning, pp. 194-195
