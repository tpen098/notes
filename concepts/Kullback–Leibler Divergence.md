---
aliases: [Relative Entropy]
tags: [statistics-probability]
date created: Sunday, November 13th 2022, 9:23:37 pm
date modified: Friday, August 21st 2026, 9:58:20 am
---

# Kullback–Leibler Divergence

## Definition

The [[Kullback–Leibler Divergence]] or [[Kullback–Leibler Divergence|Relative Entropy]] between two [[Probability|Probability Distribution]] [[Function|Functions]] $P(x), G(x)$ that are defined in the same [[Sample Space]] is defined as the [[Mean]] of the [[Entropy]] of $P(x)$ minus $Q(x)$

$$
D_{KL}(P\mid\mid Q)
= \sum_{x}P(x)\log\left( \frac{P(x)}{Q(x)} \right)
$$

> [!NOTE] Lower Bounds
> The [[Gibbs’ Inequality]] states that the [[Kullback–Leibler Divergence|Relative Entropy]] is always greater or equal to zero.

## References

1. Information theory, inference, and learning algorithms, p. 46
