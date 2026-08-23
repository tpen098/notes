---
aliases:
  - Beta-Binomial
tags:
  - statistics-probability
date created: Tuesday, November 8th 2022, 3:52:48 pm
date modified: Thursday, August 20th 2026, 6:16:30 pm
---

# Beta-Binomial Conjugacy

## Definition

Consider a [[Binomial Distribution]] $x \sim Bin(N, \mu)$, defined as follows

$$
p(x|N, mu) = {N \choose x} \mu^{x} (1-\mu)^{N-x}
$$

If a [[Beta Distribution]] was set as the _prior_ on parameter $\mu \sim Beta(\alpha, \beta)$, defined with the [[Gamma Function]] as the following:

$$
p(\mu|\alpha, \beta) =
\dfrac{\Gamma(\alpha + \beta)}
	 {\Gamma(\alpha) \Gamma(\beta)}
mu^{\alpha-1}(1-\mu)^{\beta-1}
$$

The _posterior_ by [[Conjugate Prior|Conjugacy]] can be computed as the following

$$
\begin{align}
p(\mu|x=x_{i}, N, \alpha, \beta)
&\propto
p(x|N, \mu)p(\mu| \alpha, \beta) \\
&\propto
\mu^{x_{i}}(1-\mu)^{(N-x_{i})}
\mu^{\alpha-1}(1-\mu)^{\beta-1} \\
&=
\mu^{x_{i}+\alpha-1}
(1-\mu)^{(N-x_{i})+\beta-1} \\
&= \mu Beta(x_{i}+\alpha, N-x_{i}+\beta)
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 208-209
