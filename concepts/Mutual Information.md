---
aliases: []
tags: [statistics-probability]
date created: Monday, September 19th 2022, 6:39:05 pm
date modified: Friday, August 21st 2026, 2:15:47 pm
---

# Mutual Information

## Definition

Given two [[Random Variable|Random Variables]] $X, Y$, the [[Mutual Information]] measures the [[Mean|Average]] reduction in [[Entropy|Uncertainty]] about one of the [[Random Variable|Random Variables]] if the other is given. It is defined using the individual [[Entropy]] of the first [[Random Variable]] minus the [[Conditional Entropy]] given the second [[Random Variable]], defined as the following

$$
I(X;Y) = H(X) - H(X|Y) = H(Y) - H(Y|X) = I(Y;X)
$$

It also follows from [[Bayes' Theorem]]

## General Bounds

$$0 \leq I(X, Y) \leq \min \{H(X), H(Y)\}$$

## Independent Events

If the [[Random Variable|Random Variables]] $X, Y$ are [[Statistical Independence|Statistically Independent]], then their [[Mutual Information]] is zero as knowing the other doesn't provide a change of [[Entropy]] to the other [[Random Variable]]

$$
\begin{align}
I(X;Y) = I(Y;X)
&= H(X) - H(X|Y) \\
&= H(X) - H(X) \\
&= 0 \\
I(X;Y) = I(Y;X)
&= H(Y) - H(Y|X) \\
&= H(Y) - H(Y) \\
&= 0 \\
\end{align}
$$

## References

1. [_Introduction to Information Theory Part 1_ by Charleston Dale Ambatali](https://www.youtube.com/watch?v=T6FUNttz2Ss)
2. [_Introduction to Information Theory Part 2_ by Charleston Dale Ambatali]([https://www.youtube.com/watch?v=twzLpppO6ug)
3. Information theory, inference, and learning algorithms, p. 151
