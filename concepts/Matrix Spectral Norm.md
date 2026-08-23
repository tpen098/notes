---
aliases: [Matrix Spectral Norm, Matrix Spectral Norms, Spectral Norm, Spectral Norms]
tags: [linear-algebra]
date created: Thursday, October 20th 2022, 11:49:35 am
date modified: Friday, August 21st 2026, 2:01:02 pm
---

# Matrix Spectral Norm

## Definition

---

For $x \in \mathbb{R}^n \setminus \{ 0 \}$, the [[Matrix Spectral Norm|Spectral Norm]] of a [[Matrix]] $A \in \mathbb{R}^{m \times n}$ is defined as follows

$$
\lVert A \rVert_2
:= \max_x{\dfrac{\lVert A x \rVert_2}{\lVert x \rVert_2}}
$$

## Singular Value Maximum

The [[Matrix Spectral Norm]] of a [[Matrix]] $A$ is the largest _singular value_ of its [[Singular Value Matrix]].

## References

1. Mathematics for Machine Learning, Ch.4, p. 131
