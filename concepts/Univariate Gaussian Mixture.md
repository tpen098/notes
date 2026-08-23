---
aliases: [Mixture Density]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 9:30:06 pm
date modified: Friday, August 21st 2026, 3:41:52 pm
---

# Univariate Gaussian Mixture

## Univariate Gaussian Mixture Form

Consider the following mixture of two, univariate [[Gaussian Distribution|Gaussian Distributions]] with different parameters $(\mu_{1}, \sigma_{1}^2) \neq (\mu_{2}, \sigma_{2}^2)$, but using the same scalar $0 < \alpha < 1$

$$
p(x) = \alpha p_{1} (x) + (1 - \alpha)p_{2}(x)
$$

## Mean

The [[Mean]] of the [[Univariate Gaussian Mixture|Mixture Density]] $p(x)$ is the weighted sum of the [[Mean|Means]] of each [[Random Variable]] as derived in the following

$$
\begin{align}
\mathbb{E}[x]
&= \int_{-\infty}^{\infty} x p(x) \, dx \\
&= \int_{-\infty}^{\infty} (\alpha xp_{1}(x) + (1-\alpha) xp_{2}(x)) \, dx \\
&= \alpha \int_{-\infty}^{\infty} xp_{1}(x) \, dx +
(1-\alpha)\int_{-\infty}^{\infty} xp_{2}(x) \, dx \\
&= \alpha \mu_{1} + (1-\alpha) \mu_{2}
\end{align}
$$

## Variance

The [[Variance]] of the [[Univariate Gaussian Mixture|Mixture Density]] $p(x)$ is given as the following (as derivable from the [[Mean]] by the definition of the [[Variance]])

$$
\mathbb{V}[x] = 
[\alpha \sigma_{1}^2 + (1-\alpha)\sigma_{2}^2] +
([\alpha \mu_{1}^2 + (1-\alpha)\mu_{2}^2]
-[\alpha \mu_{1} + (1 - \alpha)\mu_{2}]^2)
$$

## References

1. Mathematics for Machine Learning, pp. 202-203
