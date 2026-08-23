---
aliases:
  - Transitive
  - Transitive Relations
tags:
  - mathematics
date created: Wednesday, March 13th 2024, 10:17:29 am
date modified: Wednesday, March 13th 2024, 10:33:07 am
---

## Definition

A [[Binary Relation]] $R \subseteq A \times A$ is [[Transitive Relation|Transitive]] if for $a, b, c \in A$, $a \; R \; b$ and $b \; R \; c$ implies $a \; R \; c$ [^1]

$$
\forall a, b, c \in A: (a, b), (b, c) \in R \implies (a, c) \in R
$$

> [!example]
> An example of a [[Transitive Relation|Transitive]] [[Binary Relation]], the operators $=, \lt, \gt, \leq, \geq$ are [[Transitive Relation|Transitive]]. An example of a [[Binary Relation]] that is not [[Transitive Relation|Transitive]] is $R = \{ (a, b): a, b \in \mathbb{N}, a = b - 1 \}$ because $3 \; R \; 4$ and $4 \; R \; 5$ does not imply $3 \; R \; 5$ since $3 \neq 5 - 1$

## References

[1]: Introduction to Algorithms, p. 1159
