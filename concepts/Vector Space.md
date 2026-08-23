---
aliases: [Vector Spaces, Vector, Vectors]
tags: [linear-algebra]
date created: Thursday, September 15th 2022, 8:09:04 pm
date modified: Friday, August 21st 2026, 3:43:07 pm
---

# Vector Space

## Conditions

A real-valued vector space $V = (\mathcal{V}, +, \cdot)$ is a set $\mathcal{V}$ with two operations (inner and outer operations respectively)

$$
\begin{align}
	+&:\mathcal{V} \times \mathcal{V} \rightarrow \mathcal{V} \\
	\cdot&: \mathbb{R} \times \mathcal{V} \rightarrow \mathcal{V}
\end{align}
$$

if the following properties also hold

### Abelian

$(\mathcal{V}, +)$ must be an [[Abelian Group#Abelian Group|Abelian Group]]

### Distributivity

$$
\begin{align}
	\forall \lambda \in \mathbb{R}, x, y \in \mathcal{V}:
	\lambda \cdot (x+y) = \lambda \cdot x + \lambda \cdot y
	\\
	\forall \lambda, \psi \in \mathbb{R}, x \in \mathcal{V}:
	(\lambda+\psi)\cdot x = \lambda \cdot x + \psi \cdot x
\end{align}
$$

### Associativity with Outer Operation

$$
\forall \lambda, \psi \in \mathbb{R}, x \in \mathcal{V}: \lambda \cdot (\psi \cdot x) = (\lambda \psi) \cdot x
$$

### Neutral Element with Outer Operation

$$
\forall x \in \mathcal{V}: 1 \cdot x = x
$$

> [!note]
> Elements $x \in \mathcal{V}$ are called vectors. The inner operation here is called vector addition and elements $\lambda \in \mathbb{R}$ are called scalars.

## Examples

1. $\mathcal{V} = \mathbb{R}^n, n\in \mathbb{N}$ is a vector space with component wise addition and scaling
2. $\mathcal{V} = \mathbb{R}^{(m \times n)}, m, n \in \mathbb{N}$ is a vector space with [[Matrix Addition]] and [[Matrix Scaling]]

## References

1. Mathematics for Machine Learning, Ch.2, pp. 37-38
