---
aliases: [Random Variable Angles]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 7:26:26 pm
date modified: Sunday, August 23rd 2026, 11:55:13 am
---

# Random Variable Angle

## Definition

The [[Angle]] between two [[Random Variable|Random Variables]] $X, Y$, can be determined using the [[Random Variable Inner Product]] of the two over the product of their [[Random Variable Length]]. This ends up being the [[Correlation]] of the two [[Random Variable|Random Variables]] as shown in the following

$$
\cos\theta
= \frac{\langle X, Y \rangle}
	   {\lVert X \rVert \lVert Y \rVert}
= \frac{Cov[x, y]}
	   {\sqrt{ \mathbb{V}_{X}[x]\mathbb{V}_{Y}[y] }}
= corr[x, y]
$$

## References

1. Mathematics for Machine Learning, p. 196
