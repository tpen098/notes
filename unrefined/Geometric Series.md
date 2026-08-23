---
aliases: []
tags:
  - mathematics
date created: Thursday, September 15th 2022, 2:07:32 pm
date modified: Friday, August 21st 2026, 9:41:54 am
---

# Geometric Series

## Definition

The [[Geometric Series]] is simply the sum of terms from a [Geometric Sequence](super%20scratch/scratch/Geometric%20Sequence.md).

$$
	\sum_{k=1}^{n} a_1 r^{k-1} = a \dfrac{1-r^n}{1-r}
$$

## Different Starting Point

If $k$ were to begin at a different value, then the formula alters to the following:

$$
	\sum_{k=m}^{n} a_1 r^{k} = a \dfrac{r^m - r^{n+1}}{1-r}
$$

> [!NOTE]+
> Setting the prior formula with $m=1$ reverts the problem back to the initial form.

## Common Ratio is One

If the common ratio is set to $r=1$, the formula simplifies to:

$$
	\sum_{k=m}^{n} a_1 r^{k-1} = a (n - m + 1)
$$

## Convergence

An infinite [[Infinite Geometric Series]] will converge to the following formula if the [[Absolute Value]] of the [[Geometric Sequence|Common Ratio]] is less than 1.

$$
	\sum_{k=0}^{\infty} a_1 r^{k} = \dfrac{a}{1-r}, |r| < 1
$$

## References

1. Lorem
