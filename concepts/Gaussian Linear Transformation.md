---
aliases: [Gaussian Linear Transformations]
tags: [statistics-probability]
date created: Wednesday, November 9th 2022, 5:24:16 pm
date modified: Thursday, August 20th 2026, 6:55:52 pm
---

# Gaussian Linear Transformation

## Linear Transformation

Given a [[Gaussian Distribution|Gaussian]] [[Random Variable]] $X \sim \mathcal{N}(\mu, \Sigma)$ and a [[Matrix]] $A$, the [[Random Variable]] $Y$ defined by the transformation $y = Ax$, the [[Mean]] and [[Variance]] can be computed as shown in the following

$$
\mathbb{E}[y]
= \mathbb{E}[Ax]
= A\mathbb{E}[x]
= A\mu
\atop
\mathbb{V}[y]
= \mathbb{V}[Ax]
= A\mathbb{V}[x] A^{\top}
= A\Sigma A^{\top}
$$

This shows that the [[Random Variable]] $Y$ is also [[Gaussian Distribution|Gaussian]]

$$
p(y) = \mathcal{N}(y|A\mu, A \Sigma A^{\top})
$$

## Reverse Linear Transformation

Given a [[Matrix]] $A$ and a [[Gaussian Distribution|Gaussian]] [[Random Variable]] $Y \sim \mathcal{N}(A\mu, \Sigma)$, the [[Probability Density Function]] $p(x)$ can be defined by using $x=A^{-1}y$ and applying the rules for [[#Linear Transformation]].

However, since $A$ is not always invertible, both sides must be multiplied by $A^{\top}$ to make it into a [[Symmetric Positive Definite|Symmetric Positive Definite Matrix]] $AA^{\top}$ and then invert that.

$$
y = Ax \Leftrightarrow (AA^{\top})^{-1}A^{\top}y=x
$$

This leads to the following [[Probability Density Function]]

$$
p(x) = \mathcal{N}
(x|(A^{\top}A)^{-1}A^{\top}y,
(A^{\top}A)^{-1}A^{\top} \Sigma A (A^{\top}A)^{-1})
$$

## References

1. Mathematics for Machine Learning, pp. 198-204
