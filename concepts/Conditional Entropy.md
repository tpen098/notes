---
aliases: [Conditional Entropies]
tags: [statistics-probability]
date created: Monday, September 19th 2022, 7:22:00 pm
date modified: Sunday, August 16th 2026, 10:59:28 pm
---

# Conditional Entropy

## Definition

Given that a [[Random Variable]] $X$ takes a specific value $X=x$, then the [[Entropy]] of a [[Random Variable]] $Y$ that's assumed to be dependent on $X$ is defined as the following

$$
H(Y|X = x)
	= - \sum_{y \in Y} P(Y = y| X = x) \log{P(Y = y| X = x)}
$$

The [[Mean|Average]] for all possible values $x \in X$, the [[Conditional Entropy]] of $Y$ given $X$ is defined as the following

$$
H(Y|X)
	= - \sum_{x \in X} P(x) \log{P(Y|X = x)}
$$

## General Bounds

The [[Conditional Entropy]] is maximized when the [[Random Variable|Random Variables]] $X, Y$ have [[Statistical Independence]] which leads to a value $H(X)$.

$$
0 \leq H(X|Y) \leq H(X)
$$

## References

1. [_Introduction to Information Theory Part 1_ by Charleston Dale Ambatali](https://www.youtube.com/watch?v=T6FUNttz2Ss)
2. Information theory, inference, and learning algorithms, p. 150
