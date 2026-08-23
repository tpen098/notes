---
aliases: [Vector Subspaces]
tags: [mathematics]
date created: Thursday, September 15th 2022, 9:10:38 pm
date modified: Thursday, August 20th 2026, 6:33:47 pm
---

# Vector Subspace

## Statement

Let $V = (\mathcal{V}, +, \cdot)$ be a [[Vector Space]] and $\mathcal{U} \subseteq \mathcal{V}, \mathcal{U} \neq \emptyset$, then $U = (\mathcal{U}, +. \cdot)$ is a [[Vector Subspace]] of $V$ with vector space operations $(+. \cdot)$ restricted to $\mathcal{U} \times \mathcal{U}$ and $\mathbb{R} \times \mathcal{U}$

### Not Null

$$
\mathcal{U} \neq \emptyset: \bf{0} \in \mathcal{U}
$$

### Closure

With respect to the outer operation:

$$
\forall \lambda \in \mathbb{R}, \forall x \in \mathcal{U}:
	\lambda x \in \mathcal{U}
$$

With respect to the inner operation:

$$
\forall x, y \in \mathcal{U}:
	x + y \in \mathcal{U}
$$

## Inheritance of Properties

The vector subspace naturally inherits many properties directly from the vector subspace as they hold for all $x \in \mathcal{U} \subseteq \mathcal{V}$
- Abelian Group Properties
- Distributivity
- Associativity
- Neutral Element

## References

1. Mathematics for Machine Learning, Ch.2, pp. 39-40
