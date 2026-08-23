---
aliases: [Groups]
tags: [mathematics]
date created: Thursday, September 15th 2022, 8:10:07 pm
date modified: Thursday, August 20th 2026, 7:04:57 pm
---

# Group

## Conditions

Consider a [[Set]] $\mathscr{G}$, and an operation $\otimes: \mathscr{G} \times \mathscr{G} \rightarrow \mathscr{G}$ defined on $\mathscr{G}$, then $G := (\mathscr{G}, \otimes)$ is called a [[Group]] if the following hold:

### Closure

$$
\forall x,y \in \mathscr{G}:
x \otimes y \in \mathscr{G}
$$

### Associativity

$$
\forall x,y, z \in \mathscr{G}:
(x \otimes y) \otimes z = x \otimes (y \otimes z)
$$

### Neutral Element

$$
\exists e \in \mathscr{G}, \forall x \in \mathscr{G}:
x \otimes e = x \text{ and } e \otimes x = x
$$

### Inverse Element

$$
\forall x \in \mathscr{G}, \exists y \in G:
x \otimes y = e \text{ and } y \otimes x = e
$$

[[Abelian Group]]
### Examples

1. $(\mathbb{Z}, +)$ is an [[Abelian Group]]
2. $(\mathbb{N}_0, +)$ is not a [[Group]] since it doesn't have inverse elements
3. $(\mathbb{Z}, \cdot)$ is not a [[Group]] since inverse elements for any $z \in \mathbb{Z}, z \neq \pm 1$ are missing
4. $(\mathbb{R}, \cdot)$ is not a [[Group]] since $0$ does not have an inverse element
5. $(\mathbb{R} \text{ except } 0, \cdot)$ is an [[Abelian Group]]
6. $(\mathbb{R}^n, +), (\mathbb{Z}^n,+), n \in \mathbb{N}$ are [[Abelian Group|Abelian Groupness]] if $+$ is defined component wise (similar to [[Matrix Addition]])
7. $(R^{(m \times n)}, +)$ is an [[Abelian Group]] with component wise addition
8. $(R^{(n \times n)}, \cdot)$ is a [[Group]], specifically a [[General Linear Group]]

## References

1. Mathematics for Machine Learning, Ch.2, pp. 36-37
