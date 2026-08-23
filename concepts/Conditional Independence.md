---
aliases: [Conditionally Independent]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 6:32:45 pm
date modified: Sunday, August 16th 2026, 11:00:04 pm
---

# Conditional Independence

## Definition

Two [[Random Variable|Random Variables]] $X, Y$ are [[Conditional Independence|Conditionally Independent]] given $Z$, written as $X \perp\!\!\!\perp Y | Z$, if and only if the following holds

$$
p(x, y|z) = p(x|z)p(y|z) \forall z \in \mathcal{Z}
$$

Where $\mathcal{Z}$ is the set of states of [[Random Variable]] $Z$.

## Conditional Probability

The [[Conditional Probability Density Function|Conditional PDF]], [[Conditional Cumulative Distribution Function|Conditional CDF]], or [[Conditional Probability Mass Function|Conditional PMF]] of [[Random Variable|Random Variables]] $X, Y$, given [[Conditional Independence]] with [[Random Variable]] $Z$, can be redefined as the following

$$
p(x|y, z) = p(x|z)
\atop
p(y|x, z) = p(y|z)
$$

## Statistical Independence

The standard [[Statistical Independence]] is a special case of [[Conditional Independence]] wherein $\mathcal{Z} = \emptyset$

## References

1. Mathematics for Machine Learning, p. 195
