---
tags: [linear-algebra]
aliases: [Identity Matrices]
date created: Wednesday, October 19th 2022, 12:28:31 pm
date modified: Sunday, August 23rd 2026, 11:52:51 am
---

# Identity Matrix

## Definition

---

An [[Identity Matrix]] is a [[Square Matrix]] wherein all diagonal elements of the [[Matrix]] have a value of 1 and all other entries are 0

$$
I_n = [\delta_{ij}]:
\begin{cases}
	 \delta_{ij} = 1 & i = j\\
	 \delta_{ij} = 0 & i \neq j\\
\end{cases}
$$

$$I_n =
\begin{bmatrix}
	1 & 0 & 0 & \ldots & 0 \\
	0 & 1 & 0 &\ldots & 0 \\
	0 & 0 & 1 & \ldots & 0 \\
	\vdots & \vdots & \ddots &\ddots & \vdots \\
	0 & 0 & 0 &\ldots & 1
	\end{bmatrix}
$$

## Trace of the Identity Matrix

The [[Matrix Trace]] of the Identity Matrix is equal to its dimension

$$tr(I_n)=n$$

## References

1. Mathematics for Machine Learning, Ch.2, p. 104
