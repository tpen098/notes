---
aliases: [Parameter-Based Linear Regressions, MAP]
tags: [statistics-probability, machine-learning]
date created: Saturday, November 26th 2022, 7:39:14 pm
date modified: Friday, August 21st 2026, 2:23:00 pm
---

# Parameter-Based Linear Regression (MAP)

## Motivation

For a known [[Dataset]], the [[Bayes' Theorem|Posterior]] $p(\theta|\mathcal{X,Y})$ can be determined using [[Bayes' Theorem]]

$$
p(\theta|\mathcal{X,Y}) = \frac{
p(\mathcal{Y|X, \theta})
p(\theta)}
{p(\mathcal{Y|X})}
$$

## Parameter Estimation

Applying [[Maximum A Posteriori Principle|Maximum A Posteriori Estimation]], the [[Maximum Likelihood Estimation|Negative-Log]] of the [[Bayes' Theorem|Prior Knowledge]] and [[Bayes' Theorem|Likelihood Function]] must be minimized with respect to the parameters $\theta$. Thus, the [[Partial Derivative|Gradient]] of the [[Maximum Likelihood Estimation|Negative-Log]] of the [[Bayes' Theorem|Posterior]] must be the zero vector.

$$
\frac{d}{d\theta} (-\log(p(\theta|\mathcal{X, Y})))
= \frac{d}{d\theta} (-\log(p(\mathcal{Y|X, \theta})))
- \frac{d}{d\theta} (-\log(p(\theta))) = 0^{\top}
$$

With a [[Conjugate Prior]] $p(\theta) = \mathcal{N}(0, b^2 I)$, and using the derivation in [[Parameter-Based Linear Regression (MLE)]] for the [[Bayes' Theorem|Likelihood Function]], the [[Partial Derivative|Gradient]] can be evaluated further to obtain the optimal parameters $\theta_{ML}$

$$
\begin{align}
\frac{d}{d\theta} (-\log(p(\theta|\mathcal{X, Y})))
&= \frac{1}{\sigma^2}(\theta^{\top}\Phi^{\top}\Phi-y^{\top}\Phi)
+ \frac{1}{b^2}\theta ^{\top} = 0^{\top} \\
0^{\top}
&= \theta^{\top}
\left( \frac{1}{\sigma^2} \Phi ^{\top} \Phi+ \frac{1}{b^2}I\right)
- \frac{1}{\sigma^2} y^{\top}\Phi \\
y^{\top}\Phi
&= \theta^{\top} \left( \Phi ^{\top}\Phi+\frac{\sigma^2}{b^2}I \right) \\
\theta ^{\top}
&= y^{\top}\Phi \left( \Phi ^{\top}\Phi+\frac{\sigma^2}{b^2}I \right)^{-1} \\
\theta_{ML}
&= \left( \Phi ^{\top}\Phi+\frac{\sigma^2}{b^2}I \right)^{-1} \Phi ^{\top} y
\end{align}
$$

## Regularization Term

The [[Maximum Likelihood Estimation|Negative-Log]] of the [[Bayes' Theorem|Prior Knowledge]] functions as a [[Regularization|Regularizer]]. The term $\dfrac{\sigma^2}{b^2}I$ is the only difference of the [[Parameter-Based Linear Regression (MAP)]] with [[Parameter-Based Linear Regression (MLE)]]. It serves to adjust the [[Machine Learning Model|Model]] such that it generalizes and minimizes [[Model Fitting|Overfitting]].

## References

1. Mathematics for Machine Learning, pp. 300-303
