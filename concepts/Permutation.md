---
aliases:
  - Permutations
tags:
  - mathematics
date created: Wednesday, March 13th 2024, 11:52:33 am
date modified: Wednesday, March 13th 2024, 12:03:10 pm
---

## Definition

A [[Permutation]] of a finite [[Set]] $S$ is a [[Finite Sequence]] of all of the [[Set Membership|Elements]] of $S$, with each [[Set Membership|Element]] only appearing once [^1]

> [!example]
> Given a [[Set]] $S = \{ a, b, c \}$ then $S$ has six possible [[Permutation|Permutations]] 
> 
> $$
> abc, acb, bac, bca, cab, cba
> $$ 

Furthermore, a [[Permutation]] can have a length $k$ smaller than the [[Set Cardinality|Cardinality]] of the [[Set]] $n = \lvert S \rvert$ [^1]

> [!example]
> Given a [[Set]] $S = \{ a, b, c \}$ then $S$ has twelve possible [[Permutation|Permutations]] of length $k=2$
> 
> $$
> ab, ac, ad, ba, bc, bd, ca, cb, cd, da, db, dc
> $$

## Possible Variations

For a given [[Set]] $S$ of length $n$, the number of possible [[Permutation|Permutations]] $p$ with length $k$ is defined as the following [^1]

$$
p = \frac{n!}{(n - k)!}
$$

## References

[1]: Introduction to Algorithms, pp. 1179-1180
