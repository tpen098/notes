---
aliases:
  - Bernoulli
tags:
  - statistics-probability
date created: Monday, November 7th 2022, 5:36:54 pm
date modified: Sunday, August 16th 2026, 4:00:23 pm
---

# Bernoulli Distribution

## Definition

The [[Bernoulli Distribution]] is a [[Probability Mass Function]] for a single binary [[Random Variable]] $X$ with state $x \in \{ 0, 1 \}$. It is mainly described by a single, continuous parameter $\mu \in [0, 1]$ that represents $X=1$

$$
p(x|\mu) = \mu^x (1-\mu)^{1-x}
$$

## Mean

The [[Mean]] of a [[Bernoulli Distribution]] is equal to its describing parameter $\mu$ as shown in the following

$$
\mathbb{E}[x] = \mu
$$

## Variance

The [[Variance]] of a [[Bernoulli Distribution]] is equal to the product of parameter $\mu$ by $(1-\mu)$ as shown in the following

$$
\mathbb{V}[x] = \mu (1-\mu)
$$

## Exponential Family Representation

Consider a [[Bernoulli Distribution]] described as the following

$$
p(x|\mu) = \mu^x (1-\mu)^{1-x}, x \in \{ 0, 1 \}
$$

The expression can be rewritten as a member of the [[Exponential Family]] as shown in the following

$$
\begin{align}
p(x|\mu)
&= \exp(\log(\mu^x (1-\mu)^{1-x})) \\
&= \exp(x \log(\mu)+(1-x)\log(1-\mu))) \\
&= \exp(x \log(\mu)-x\log(1-\mu)+\log(1-\mu))) \\
&= \exp\left( x\log\left( \frac{\mu}{1+\mu} \right) + \log(1-\mu) \right)
\end{align}
$$

The properties of the [[Exponential Family]] are listed as follows

$$
\begin{align}
h(x) &= 1 \\
\theta &= \log\left( \frac{\mu}{1-\mu} \right) \\
\phi(x) &= x \\
A(\theta) &= -\log (1-\mu) = \log(1+ \exp(\theta))
\end{align}
$$

### Sigmoid Function

The original $\mu$ parameter relates to $\theta$ using the [[Sigmoid Activation Function]] as shown in the following. This effectively squeezes a real value $\theta \in \mathbb{R}^D$ to the limits of $\mu \in [0, 1]$

$$
\mu = \frac{1}{1+\exp(-\theta)}
$$

## Reference

1. Mathematics for Machine Learning, pp. 205-206, 212-213
