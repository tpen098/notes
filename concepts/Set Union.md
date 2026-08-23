---
aliases:
  - Set Unions
  - Union
  - Unions
tags:
  - mathematics
date created: Tuesday, March 12th 2024, 5:05:06 am
date modified: Tuesday, March 12th 2024, 6:23:29 pm
---

## Definition

The [[Set Union]] between two [[Set|Sets]] $A, B$ is defined as the [[Set]] wherein the [[Set Membership|Elements]] are [[Set Membership|included]] in either [[Set|Sets]] [^1]

$$
A \cup B = \{ x: x \in A \text{ or } x \in B\}
$$

## Operation Laws

### Empty Set Law

Given a [[Set]] $\mathcal{S}$ and an [[Null Set|Empty Set]] $\emptyset$, the[[Set Union]] of the two [[Set|Sets]] is the given [[Set]] $\mathcal{S}$[^1]

$$
\mathcal{S} \cup \emptyset = \mathcal{S}
$$

### Idempotency Law

Given a [[Set]] $\mathcal{S}$, the [[Set Union]] of the [[Set]] with itself is also itself $\mathcal{S}$ [^1]

$$
\mathcal{S} \cup \mathcal{S} = \mathcal{S}
$$

### Commutative Law

Given two [[Set|Sets]] $A, B$, their order in a [[Set Union]] does not matter [^1]

$$
A \cap B = B \cap A
$$

### Associative Law

Given three [[Set|Sets]] $A, B, C$, the order of their [[Set Union]] does not matter [^1]

$$
A \cup (B \cup C) = (A \cup B) \cup C
$$

### Distributive Law

Given three [[Set|Sets]] $A, B, C$, the [[Set Union]] operation can be distributed to a [[Set Intersection]] [^1]

$$
A \cup (B \cap C) = (A \cup B) \cap (A \cup C)
$$

### Absorption Law

Given two [[Set|Sets]] $A, B$, the [[Set Union]] of $A$ with the [[Set Intersection]] $A \cap B$ results to $A$ [^1]

$$
A \cup (A \cap B) = A
$$

### De Morgan's Law

Given three [[Set|Sets]] $A, B, C$, the [[Set Difference]] of $A$ with the [[Set Union]] $B \cap C$ can be distributed to $B, C$ individually by inverting the [[Set Union]] to [[Set Intersection]] [^1]

$$
A - (B \cup C) = (A - B) \cap (B - C)
$$

Using the [[Set Complement]] definition, the [[#De Morgan's Law]] can be redefined as the distribution of the [[Set Complement]] to the individual [[Set|Sets]] of a [[Set Union]] by converting it into a [[Set Intersection]] [^1]

$$
\overline{B \cup C} = \bar{B} \cap \bar{C}
$$

## References

[1]: Introduction to Algorithms, p. 1154-1156
