---
aliases:
  - Marginalization
tags:
  - statistics-probability
date created: Sunday, August 16th 2026, 3:58:49 pm
date modified: Friday, August 21st 2026, 3:31:09 pm
---

# Sum Rule

## Marginal Probability Mass Function via Joint Probability Mass Function

For [[Random Variable|Random Variables]] $X = \{ X_{1}, \dots, X_{D}\} \in \mathbb{R}^D$ in a Discrete [[Target Space]], the [[Marginal Probability Mass Function]] $p(x_{i})$ can be defined as sequential summations of the [[Joint Probability Mass Function]] $p(x_{1}, \dots, x_{n})$ with respect to every [[Target Space]] except $\mathcal{T}_{i}$

$$ p(x_{i}) =
\sum_{X_{n}}
\dots
\sum_{X_{1}}
p(x_{1}, \dots, x_{n}) $$

Where the summations are over all points in the range of $X = \{ X_1,\dots, X_{n} \} \setminus \{ X_{i} \}$ where $X_{i} = x_{i}$

## Marginal Cumulative Distribution via Joint Cumulative Distribution


For [[Random Variable|Random Variables]] $X = \{ X_{1}, \dots, X_{D}\} \in \mathbb{R}^D$ in a Continuous [[Target Space]], the [[Marginal Cumulative Distribution Function]] $p(x_{i})$ can be defined as sequential integrations of the [[Joint Cumulative Distribution Function]] $p(x_{1}, \dots, x_{n})$ with respect to every [[Target Space]] except $\mathcal{T}_{i}$

$$ p(x_{i}) =
\int
\dots
\int
p(x_{1}, \dots, x_{n})
\;
d_{x_{1}} \dots d_{x_{i-1}} d_{x_{i+1}} \dots d_{x_{n}}
$$

Where the integrations are all over points in the range $X = \{ X_1,\dots, X_{n} \} \setminus \{ X_{i} \}$ where $X_{i} = x_{i}$

## Marginal Probability Density Function via Joint Probability Density Distribution

For [[Random Variable|Random Variables]] $X = \{ X_{1}, \dots, X_{D}\} \in \mathbb{R}^D$ in a Continuous [[Target Space]], the [[Marginal Probability Density Function]] $p(x_{i})$ can be defined as sequential integrations of the [[Joint Probability Density Function]] $p(x_{1}, \dots, x_{n})$ with respect to every [[Target Space]] except $\mathcal{T}_{i}$

$$ p(x_{i}) =
\int
\dots
\int
p(x_{1}, \dots, x_{n})
\;
d_{x_{1}} \dots d_{x_{i-1}} d_{x_{i+1}} \dots d_{x_{n}}
$$

Where the integrations are all over points in the range $X = \{ X_1,\dots, X_{n} \} \setminus \{ X_{i} \}$ where $X_{i} = x_{i}$

## References

1. Mathematics for Machine Learning, pp. 184
2. Applied Statistics and Probability for Engineers, p. 108
