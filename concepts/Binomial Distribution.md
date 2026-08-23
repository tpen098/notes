---
aliases: [Binomial, Binomial Distributions]
tags: [statistics-probability]
date created: Monday, November 7th 2022, 5:44:35 pm
date modified: Sunday, August 16th 2026, 9:16:44 pm
---

# Binomial Distribution

## Definition

---

The [[Binomial Distribution]] is a [[Probability Mass Function]] that generalizes the [[Bernoulli Distribution]] to a distribution over integers (as opposed to being binary). It describes the probability of observing $m$ occurrences of $X=1$ in a set of $N$ samples from a [[Bernoulli Distribution]]. It is defined as the following:

$$
p(m|N, mu) = {N \choose m} \mu^{m} (1-\mu)^{N-m}
$$

## Mean

The [[Mean]] of a [[Binomial Distribution]] is equal to its describing parameter $\mu$ times by $N$ shown in the following

$$
\mathbb{E}[m] = N\mu
$$

## Variance

The [[Variance]] of a [[Binomial Distribution]] is equal to the product of parameter $\mu$ by $(1-\mu)$ times $N$ as shown in the following

$$
\mathbb{V}[m] = N \mu (1-\mu)
$$

## References

1. Mathematics for Machine Learning, p. 206
