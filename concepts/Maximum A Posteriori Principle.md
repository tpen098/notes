---
aliases: [Maximum A Posteriori Estimation, MAP Estimation]
tags: [statistics-probability]
date created: Sunday, November 13th 2022, 1:29:43 pm
date modified: Friday, August 21st 2026, 2:04:07 pm
---

# Maximum A Posteriori Principle

## Statement

Using [[Bayes' Theorem]], prior knowledge on the distribution of parameters $\theta$ and a given likelihood function leads to a term proportional to the posterior $p(\theta|\mathcal{D})$ Since the [[Probability]] $p(\mathcal{D})$ is not a [[Function]] that's dependent on $\theta$, it does not affect the optimization.

$$
p(\theta|\mathcal{D})
= \frac{p(\mathcal{D}|\theta)p(\theta)}{p(\mathcal{D})}
\propto p(\mathcal{D}|\theta)p(\theta)
$$

Instead of estimating the minimum of the negative log-likelihood as in [[Maximum Likelihood Estimation]], the minimum of the negative log-posterior can be estimated instead, known as the [[Maximum A Posteriori Principle|Maximum A Posteriori Estimation]] as shown

$$
\begin{align}
\log p(\theta|\mathcal{D})
&= \log(p(\mathcal{D}|\theta))
+ \log(p(\theta))
\\
arg\max_{\theta} \log(p(\theta|\mathcal{D}))
&= arg\max_{\theta} (\log(p(\mathcal{D}|\theta)) + \log(p(\theta)))
\\
arg\max_{\theta} \log(p(\theta|\mathcal{D}))
&= arg\min_{\theta} (-\log(p(\mathcal{D}|\theta)) - \log(p(\theta)))
\end{align}
$$

## Parameter as Gaussian Distribution

If the [[Probability|Probability Distribution]] of the parameter $p(\theta)$ is assumed to be a [[Gaussian Distribution]] with zero [[Mean]], then the [[Regularization]] component $-\log(p(\theta))$ becomes [[Weight Penalty Regularization]].

$$
\begin{align}
p(\theta)
= \mathcal{N}(0, \Sigma)
= -\log(p(\theta))
= \lambda\theta ^{\top}\theta
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp. 268-270
