---
aliases: [Negative-Log, Negative-Log Likelihood, Negative-Log Likelihood Function, Negative-Log Likelihood Functions, Negative-Log Function, Negative-Log Functions]
tags: [statistics-probability]
date created: Sunday, November 13th 2022, 12:26:14 pm
date modified: Friday, August 21st 2026, 2:06:01 pm
---

# Maximum Likelihood Estimation

## Definition

Given the [[Conditional Probability Mass Function]] or the likelihood function $p(x|\theta)$ that represents the probability of $x$ in an [[Independent and Identically Distributed|IID]] [[Dataset]] given parameters $\theta$, the [[Maximum Likelihood Estimation|Negative-Log Likelihood Function]] is given by

$$
\mathcal{L}_{x}(\theta) = - \log(p(x|\theta))
$$

> [!NOTE] Fixed Dataset, Varying Parameters
> The variables $x$ are implied to be constant as opposed to the parameters $\theta$ that might change. Thus, $\mathcal{L}_{x}$ can be written as $\mathcal{L}$ instead.

The [[Maximum Likelihood Estimation|Negative-Log Likelihood Function]] tells how likely the particular setting of $\theta$ is for the fixed observation $x$ from the [[Dataset]].

## Intuition for the Use of the Log Function

The [[Logarithm]] function is used as it doesn't change the location of the minima and represents very small numbers to more representable values.

Given the range of a [[Probability|Probability Distribution]] $[0, 1]$, very small values under the [[Logarithm]] will be negative so a corrective negative scaling is necessary for positive representation. This isn't a concern for the highest possible value of $1$.

## Intuition for Maximum Likelihood

The likelihood of parameters $\theta$ fitting data $x$ is at its peak when the [[Maximum Likelihood Estimation|Negative-Log Likelihood]] is at its minimum $\mathcal{L} = -\log(p(x|\theta) = 1)= 0$

Conversely, the likelihood is at its worst when the negative-log is at its maximum $\mathcal{L} = -\log(p(x|\theta) = 0) \to \infty$.

## References

1. Mathematics for Machine Learning, pp. 265-266
