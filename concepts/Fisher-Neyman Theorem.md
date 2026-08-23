---
aliases:
  - Sufficient Statistic
  - Sufficient Statistics
tags:
  - statistics-probability
date created: Wednesday, November 9th 2022, 10:11:14 am
date modified: Thursday, August 20th 2026, 6:52:33 pm
---

# Fisher-Neyman Theorem

## Definition

Let [[Random Variable]] $X$ have the [[Probability]] $p(x|\theta)$. The statistics $\phi(x)$ are sufficient for $\theta$ if and only if the probability function can be rewritten as the following

$$
p(x|\theta) = h(x)g_{\theta}(\phi(x))
$$

wherein $h(x)$ is a distribution [[Statistical Independence|Independent]] of $\theta$ and $g_{\theta}$ captures all the dependencies of $\theta$ via sufficient statistics $\phi(x)$

## Sufficient Statistics

The [[Fisher-Neyman Theorem|Sufficient Statistics]] $\phi(x)$ contains all the available information that can be inferred from data corresponding to a distribution. They sufficiently represent the distribution.

## Dependency

If $p(x|\theta)$ does not depend on $\theta$, then the [[Fisher-Neyman Theorem|Sufficient Statistics]] $\phi(x)$ is trivially a [[Fisher-Neyman Theorem|Sufficient Statistic]] for any [[Function]] $\phi$. If $p(x|\theta)$ is dependent only on $\phi(x)$ and not $x$ itself, then $\phi(x)$ is a [[Fisher-Neyman Theorem|Sufficient Statistic]] for $\theta$

## References

1. Mathematics for Machine Learning, p. 210
