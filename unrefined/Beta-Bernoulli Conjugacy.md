---
aliases:
  - Beta-Bernoulli
tags:
  - statistics-probability
date created: Tuesday, November 8th 2022, 3:40:53 pm
date modified: Tuesday, August 18th 2026, 9:20:43 pm
---

# Beta-Bernoulli Conjugacy

## Definition

Let $x \in \{ 0, 1 \}$ be distributed according to the [[Bernoulli Distribution]]

$$
p(x| \theta) = \theta^x(1-\theta)^{1-x},
\theta \in [0, 1]
$$

If the parameter $\theta$ is distributed according to a [[Beta Distribution]] with parameters $\alpha, \beta$ as shown

$$
p(\theta| \alpha, \beta)
\propto \theta^x(1-\theta)^{1-x}
$$

Then the _posterior_ by [[Conjugate Prior|Conjugacy]] can be computed as the following

$$
\begin{align}
p(\theta|x, \alpha, \beta)
&= p(x|\theta)p(\theta|\alpha, \beta) \\
&\propto
\theta^x(1-\theta)^{1-x}
\theta^{\alpha-1}(1-\theta)^{\beta-1} \\
&\propto
\theta^{\alpha+x-1} (1-\theta)^{\beta+(1-x)-1} \\
&\propto
p(\theta|\alpha + x, \beta + (1-x)) \\
&\propto
Beta (\alpha + x, \beta + (1-x))
\end{align}
$$

## References

1. Mathematics for Machine Learning, p. 209
