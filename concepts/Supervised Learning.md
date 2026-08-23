---
aliases: []
tags: [machine-learning]
date created: Sunday, November 13th 2022, 1:04:00 pm
date modified: Friday, August 21st 2026, 3:32:05 pm
---

# Supervised Learning

## Conditional Probability

Given a [[Dataset]] $\mathcal{D} = {(x_{n}, y_{n})}$, the target [[Machine Learning Model|Model]] with a conditional [[Probability]] $p(\mathcal{D}|\theta)$, assuming a linear model $x_{n}^{\top} \theta$, can be written as the following

$$
p(\mathcal{D}|\theta) \to (\hat{y}_{n}|x_{n}, \theta)
$$

Further assuming an [[Independent and Identically Distributed|IID Dataset]], the [[Machine Learning Model|Model]] can be represented as a product of [[Probability|Probabilities]] or a sum of [[Probability|Probabilities]] under [[Maximum Likelihood Estimation]].

$$
\begin{align}
p(\mathcal{D}|\theta)
&= p(\mathcal{Y}|\mathcal{X}, \theta) \\
&= \prod_{n=1}^{N} p(\hat{y}_{n}|x_{n}, \theta) \\
\\
\mathcal{L}_{\mathcal{D}}
&= -\log(p(\mathcal{Y}|\mathcal{X}, \theta)) \\
&= -\sum_{n=1}^{N} \log(p(\hat{y}_{n}|x_{n}, \theta)) \\
\end{align}
$$

## Gaussian Distribution

Assuming an [[Statistical Independence|Independent]] [[Gaussian Distribution|Gaussian]] noise with zero [[Mean]] and standard deviation $\sigma^2$ $\epsilon_{n} \sim \mathcal{N}(0, \sigma^2)$, the likelihood of each [[Model Input|Example]]-[[Model Label|Label]] pair $(x_{n}, y_{n})$ can be defined as the following

$$
p(y_{n}|x_{n}, \theta) =
\mathcal{N}(y_{n}|x_{n}^{\top}\theta, \sigma^2)
$$

Under an [[Independent and Identically Distributed|IID Dataset]], this is further expressed as the following

$$
\begin{align}
p(\mathcal{D}|\theta)
&= p(\mathcal{Y}|\mathcal{X}, \theta) \\
&= \prod_{n=1}^{N} p(\hat{y}_{n}|x_{n}^{\top}\theta, \sigma^2) \\
\\
\mathcal{L}_{\mathcal{D}}
&= -\log(p(\mathcal{Y}|\mathcal{X}, \theta)) \\
&= -\sum_{n=1}^{N} \log(p(\hat{y}_{n}|x_{n}^{\top}\theta, \sigma^2)) \\
\end{align}
$$

In full expression of the [[Gaussian Distribution]], the [[Conditional Cumulative Distribution Function|Conditional CDF]] or [[Conditional Probability Mass Function|Conditional PMF]] can be expressed as an [[Empirical Risk]] with a constant term

$$
\begin{align}
\mathcal{L}_{\mathcal{D}}(\theta)
&=
-\sum_{n=1}^{N}\log\left( \frac{1}{\sqrt{ 2\pi \sigma^2 }}
\exp\left( - \frac{(\hat{y}_{n} - x_{n}^{\top}\theta)^2}{2\sigma^2} \right)
\right) \\
&= \sum_{n=1}^{N}
\left( \frac{(\hat{y}_{n} - x_{n}^{\top}\theta)^2}{2\sigma^2} \right)
- \sum_{n=1}^{N}
 \log\left( \frac{1}{\sqrt{ 2\pi \sigma^2 }} \right)
\end{align}
$$

## Reference

1. Mathematics for Machine Learning, pp. 266-268
