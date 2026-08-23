---
aliases: [Shannon Entropy, Uncertainty, Entropies, Uncertainties, Shannon Information Content, Shannon Information Contents, Measure of Uncertainty]
tags: [statistics-probability, information-theory]
date created: Monday, September 19th 2022, 7:00:54 pm
date modified: Thursday, August 20th 2026, 10:15:58 pm
---

# Entropy

## Definition

The [[Entropy|Shannon Information Content]] or [[Entropy|Measure of Uncertainty]] from an outcome $x$ of a [[Random Variable]] $X$ is defined as the following

$$
h(x) = -\log(P(x))
$$

For a group of outcomes $x_i \in X$, the [[Entropy]] is defined using the [[Mean]] of its singular form as shown in the following

$$
H(X) = -\sum_{x \in X} P(x) \log{P(x)}
$$

## Self Mutual Information

The [[Mutual Information]] of a [[Random Variable]] $X$ with itself is its [[Entropy]]

$$I(X, X) = H(X)$$

## Bounds in Variable Change

Given a mapping of a [[Random Variable]] $X$ to another [[Random Variable]] $Y = g(X)$, the [[Entropy]] of $X$ is bound to be greater or equal to the [[Entropy]] of $Y$

$$Y = g(X): H(Y) \leq H(X)$$

## General Bounds

The [[Entropy|Uncertainty]] of an outcome $x$ is bound between $0$ (certain), or the log of the cardinality of the [[Sample Space]] $\bar{X}$

$$0 \leq H(x) \leq -\log{(c(\bar{X}))}$$

### Minimum Uncertainty

$$P(x) = 1, x \in \bar{X}: H(x) = 0$$

### Maximum Uncertainty

$$
P(x) = \dfrac{1}{c(\bar{X})} \forall x \in \bar{X}: H(x) = -\log{(c(\bar{X}))}
$$

## References

1. [_Introduction to Information Theory Part 1_ by Charleston Dale Ambatali](https://www.youtube.com/watch?v=T6FUNttz2Ss)
2. Information theory, inference, and learning algorithms, p. 44
