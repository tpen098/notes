---
tags: [linear-algebra]
aliases: [Kernel, Null Space, Kernels, Null Spaces]
date created: Friday, September 16th 2022, 1:18:06 pm
date modified: Friday, August 21st 2026, 9:58:02 am
---

# Kernel

## Definition

For the [[Linear Mapping]] $\Phi: V \rightarrow W$, the [[Kernel]] or [[Kernel|null space]] is the [[Set]] of [[Vector Space|Vectors]] $v \in V$ that $\Phi$ maps onto the neutral element $\bf{0}_W \in W$

$$
ker(\Phi) := \Phi^{-1}(0_W)
=
\{ v \in V: \Phi(v) = 0_W \}
$$

> [!note]
> The [[Kernel]] is the general solution to the [[Linear System General Solution|homogenous system of linear equations]] $Ax = 0$

## Properties

- It's always true that $\Phi(0_V) = 0_W$ so $0_V \in ker(\Phi)$. The [[Kernel|Null Space]] is never empty
- $ker(\Phi) \subseteq V$ is a [[Vector Subspace]] of $V$

## References

1. Mathematics for Machine Learning, Ch.2, pp. 58-59
