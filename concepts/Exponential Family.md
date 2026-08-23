---
aliases: [Exponential Distribution, Exponental Distributions]
tags: [statistics-probability]
date created: Wednesday, November 9th 2022, 11:08:21 am
date modified: Sunday, August 23rd 2026, 11:51:09 am
---

# Exponential Family

## Definition

---

The [[Exponential Family]] is a family of [[Probability|Probability Distribution]], parameterized by $\theta \in \mathbb{R}^D$ of the following form

$$
p(x|\theta)
= h(x)
\exp(\langle \theta, \phi(x) \rangle - A(\theta))
$$

Where $\phi(x)$ is the vector of the [[Fisher-Neyman Theorem|Sufficient Statistic]].

### Vector Product

Generally, an [[Inner Product]] can be used for an [[Exponential Family]], but the [[Dot Product]] is often used

$$
\langle \theta, \phi(x) \rangle
= \theta ^{\top} \phi(x)
$$

### Normalization Constant

The $A(\theta)$ is the _normalization constant_ called the _log-partition_ [[Function]] that ensures the distribution sums up (discrete) or integrates (continuous) to one

## Natural Parameters

When the normalization constant and $h(x)$ term is ignored, the [[Exponential Family]] takes the following form

$$
p(x|\theta) \propto \exp(\theta ^{\top} \phi(x))
$$

In this form, the $\theta$ parameters is called the _natural parameters_

## Conjugacy

---

Consider a [[Random Variable]] $X$ as a member of the [[Exponential Family]] with the following form.

$$
p(x|\theta)
= h(x)
\exp(\langle \theta, \phi(x) \rangle - A(\theta))
$$

Every member of the [[Exponential Family]] has a [[Conjugate Prior]] with the following form

$$
p(\theta|\gamma) =
h_{c}(\theta)
\exp \left(\left \langle
\begin{bmatrix}
\gamma_{1} \\ \gamma_{2} \\
\end{bmatrix},
\begin{bmatrix}
\theta \\ -A(\theta) \\
\end{bmatrix}
\right \rangle
- A_{c}(\gamma)
\right)
$$

## References

---

1. [[@Mathematics for Machine Learning]] (pp. 211-214)
