---
aliases: [Gaussian Sum]
tags: [statistics-probability]
date created: Sunday, November 6th 2022, 9:21:39 pm
date modified: Thursday, August 20th 2026, 6:57:26 pm
---

# Gaussian Sums

## Definition

The sum of two, [[Statistical Independence|Independent]], [[Gaussian Distribution|Gaussian]] [[Random Variable|Random Variables]] $X, Y$ is also a [[Gaussian Distribution]] given by the following

$$
p(x+y) =
\mathcal{N}(\mu_{x}+\mu_{y}, \Sigma_{x}+\Sigma_{y})
$$

## Weighted Sum

The weighted sum of two, [[Statistical Independence|Independent]], [[Gaussian Distribution|Gaussian]] [[Random Variable|Random Variables]] $X, Y$ is also a [[Gaussian Distribution]] by $a, b\in \mathbb{R}$ respectively is shown

$$
p(ax+by) =
\mathcal{N}
(a\mu_{x}+b\mu_{y},
a^2 \Sigma_{x} + b^2 \Sigma_{y})
$$

## References

1. Mathematics for Machine Learning, pp. 201-202
