---
aliases:
  - Intersection
  - Intersections
  - Set Intersections
tags:
  - mathematics
date created: Tuesday, March 12th 2024, 4:51:10 am
date modified: Tuesday, March 12th 2024, 6:14:17 pm
---

## Definition

The [[Set Intersection]] between two [[Set|Sets]] $A, B$ is defined as the [[Set]] wherein the [[Set Membership|Elements]] are [[Set Membership|included]] in both [[Set|Sets]] [^1]

$$
A \cap B = \{ x: x \in A, x \in B\}
$$

## Operation Laws

### Empty Set Law

Given a [[Set]] $\mathcal{S}$ and an [[Null Set|Empty Set]] $\emptyset$, the [[Set Intersection]] of the two [[Set|Sets]] is the [[Null Set|Empty Set]] [^1]

$$
\mathcal{S} \cap \emptyset = \emptyset
$$

### Idempotency Law

Given a [[Set]] $\mathcal{S}$, the [[Set Intersection]] of the [[Set]] with itself is also itself $\mathcal{S}$ [^1]

$$
\mathcal{S} \cap \mathcal{S} = \mathcal{S}
$$

### Commutative Law

Given two [[Set|Sets]] $A, B$, their order in a [[Set Intersection]] does not matter [^1]

$$
A \cap B = B \cap A
$$

### Associative Law

Given three [[Set|Sets]] $A, B, C$, the order of their [[Set Intersection]] does not matter [^1]

$$
A \cap (B \cap C) = (A \cap B) \cap C
$$

### Distributive Law

Given three [[Set|Sets]] $A, B, C$, the [[Set Intersection]] operation can be distributed to a [[Set Union]] [^1]

$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C)
$$

### Absorption Law

Given two [[Set|Sets]] $A, B$, the [[Set Intersection]] of $A$ with the [[Set Union]] $A \cup B$ results to $A$ [^1]

$$
A \cap (A \cup B) = A
$$

### De Morgan's Law

Given three [[Set|Sets]] $A, B, C$, the [[Set Difference]] of $A$ with the [[Set Intersection]] $B \cup C$ can be distributed to $B, C$ individually by inverting the [[Set Intersection]] to [[Set Union]] [^1]

$$
A - (B \cap C) = (A - B) \cup (B - C)
$$

Using the [[Set Complement]] definition, the [[#De Morgan's Law]] can be redefined as the distribution of the [[Set Complement]] to the individual [[Set|Sets]] of a [[Set Intersection]] by converting it into a [[Set Union]] [^1]

$$
\overline{B \cap C} = \bar{B} \cup \bar{C}
$$

## References

[1]: Introduction to Algorithms, pp. 1154-1556
