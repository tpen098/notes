---
aliases: [Joint Entropies]
tags: [statistics-probability]
date created: Monday, September 19th 2022, 7:14:10 pm
date modified: Sunday, August 23rd 2026, 11:53:32 am
---

# Joint Entropy

## Definition

For [[Random Variable|Random Variables]] $X_1, X_2, \ldots, X_n$, with [[Joint Probability Mass Function]] $P(X_1 \cap X_2 \cap \ldots \cap X_n) = P(X_1, X_2, \ldots, X_n)$, the _Joint [[Entropy]]_ is defined by the following

$$
H(X_1, \ldots, X_n) =
- \sum_{
  (x_1, \ldots, x_n) \in
  (\bar{X_1} \times \ldots \times \bar{X_n})
}
P(x_1, \ldots, x_n)
log P(x_1, \ldots, x_n)
$$

> [!tip]
> [[Joint Entropy]] is determining the [[Entropy]] of the entire system by determing the value of all the [[Random Variable|Random Variables]] simultaneously

## General Bounds

The maximum value of the [[Joint Entropy]] is the sum of the [[Entropy]] values of the individual [[Random Variable|Random Variables]] $X_i$ if and only if their [[Probability|Probabilities]] are [[Statistical Independence|Statistically Independent]]

$$
H(X_{1}, \dots, X_{N}) \leq \sum H(X)
$$

## Definition Using Conditional Entropy

The [[Joint Entropy]] of two [[Random Variable|Random Variables]] $X, Y$ can be defined as the sum of the first [[Random Variable]]'s [[Entropy]] and the [[Conditional Entropy]] of the second [[Random Variable]] given the first

$$
\begin{align}
H(X, Y)
&= H(X) + H(Y|X) \\
&= H(Y) + H(X|Y)
\end{align}
$$

## References

1. [_Introduction to Information Theory Part 1_ by Charleston Dale Ambatali](https://www.youtube.com/watch?v=T6FUNttz2Ss)
2. Information theory, inference, and learning algorithms, p. 45
