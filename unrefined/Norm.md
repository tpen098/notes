---
tags:
  - linear-algebra
aliases:
  - Norms
  - Length
date created: Tuesday, September 20th 2022, 12:42:29 pm
date modified: Friday, August 21st 2026, 2:16:50 pm
---

# Norm

## Statement

The [[Norm]] of a [[Vector Space]] $V$ is a [[Function]] which assigns each [[Vector Space|Vector]] $x$ its length $||x|| \in \mathbb{R}$

$$
\begin{align}
\lVert \cdot \rVert: V \rightarrow\mathbb{R} \\
x \mapsto \lVert x \rVert
\end{align}
$$

> [!TLDR] TLDR
> [[Norm]] is a measure of Length

## Absolutely Homogenous Property

$$
\lVert \lambda x \rVert =
\lvert \lambda \rvert \lVert x \rVert
$$

## Triangle Inequality Property

$$
\lVert x + y \rVert \leq
\lVert x \rVert + \lVert y \rVert
$$

## Positive Definite Property

$$
\lVert x \rVert \geq 0 \text{ and }
\lVert x \rVert = 0 \Longleftrightarrow x = 0
$$

## References

1. Mathematics for Machine Learning, Ch. 3, p. 71
