---
aliases:
  - Metrics
tags:
  - linear-algebra
date created: Tuesday, September 20th 2022, 3:43:07 pm
date modified: Friday, August 21st 2026, 2:08:09 pm
---

# Metric

## Statement

The following [[Bilinear Mapping]] is called a [[Metric]]

$$
\begin{align}
d: V \times V \rightarrow \mathbb{R} \\
(x, y) \mapsto d(x, y)
\end{align}
$$

> [!tldr] TLDR
> [[Metric]] is a measure of distance that uses an [[Inner Product|Inner Product]]

## Positive Definite Property

$$
d(x, y) \geq 0, \forall x, y \in V
$$

$$
d(x, y) = 0 \Longleftrightarrow x=y
$$

## Symmetric Property

$$
d(x, y) = d(y, x),
\forall x, y \in V
$$

## Triangle Inequality Property

$$
d(x, z) \leq d(x, z) + d(y, z),
\forall x, y, z \in V
$$

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 75-76
