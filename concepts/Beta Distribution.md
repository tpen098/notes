---
tags: [statistics-probability]
aliases: [Beta, Beta Distributions]
date created: Tuesday, November 8th 2022, 12:45:49 pm
date modified: Tuesday, August 18th 2026, 9:19:58 pm
---

# Beta Distribution

## Definition

The [[Beta Distribution]] is a [[Probability Density Function]] of a continuous [[Random Variable]] on a finite interval $\mu = [0, 1]$. The definition uses the [[Gamma Function]] as shown:

$$
p(\mu|\alpha, \beta) =
\dfrac{\Gamma(\alpha + \beta)}
	 {\Gamma(\alpha) \Gamma(\beta)}
mu^{\alpha-1}(1-\mu)^{\beta-1}
$$

## Mean

The [[Mean]] of a [[Beta Distribution]] is defined as the following

$$
\mathbb{E}[\mu] = \dfrac{\alpha}{\alpha + \beta}
$$

## Variance

The [[Variance]] of a [[Beta Distribution]] is defined as the following

$$
\mathbb{V}[\mu] =
\dfrac{\alpha\beta}
{(\alpha+\beta)^2 (\alpha + \beta + 1)}
$$

## Intuition

The [[Variable]] $\alpha$ moves the distribution towards $1$, whereas the [[Variable]] $\beta$ moves the distribution towards $0$.

### Special Cases

- For $\alpha = \beta = 1$, the [[Beta Distribution]] becomes a [[Uniform Distribution]] $\mathcal{U}[0, 1]$
- For $\alpha, \beta < 1$, the [[Beta Distribution]] spikes at $0$ and $1$
- For $\alpha, \beta > 1$, the [[Beta Distribution]] is unimodal or has one spike
- For $\alpha = \beta > 1$, the [[Beta Distribution]] is unimodal, symmetric, and centered (the [[Mean]] is $\frac{1}{2}$)

## Exponential Family Representation

Given the [[Exponential Family]] representation of the [[Bernoulli Distribution]] as shown

$$
p(x|\mu)
= \exp\left(
x\log\left(
\frac{\mu}{1+\mu} \right)
+ \log(1-\mu)
\right)
$$

The canonical [[Conjugate Prior]] will then have the following form

$$
p(\mu|\alpha, \beta)
= \frac{\mu}{1-\mu}
\exp\left(
\alpha \log\frac{\mu}{1-\mu}
+ (\beta+\alpha)\log(1-\mu)
- A_{c}(\gamma)
\right)
$$

If the following parameters are used

$$
\gamma := \begin{bmatrix}
\alpha \\ \beta+\alpha
\end{bmatrix}
\atop
h_{c}(\mu) := \begin{bmatrix}
\dfrac{\mu}{1-\mu}
\end{bmatrix}
$$

Then the [[Conjugate Prior]] expression simplifies to the following

$$
p(\mu|\alpha, \beta)
= \exp(
(\alpha-1)\log \mu
+ (\beta-1)\log(1-\mu)
- A_{c}(\alpha, \beta)
)
$$

In non-[[Exponential Family]] representation, this reverts back to

$$
p(\mu|\alpha, \beta) \propto
\mu^{\alpha-1} (1-\mu)^{\beta-1}
$$

## References

1. Mathematics for Machine Learning, pp. 206-207, 213-214
