---
tags: [linear-algebra]
aliases: [Transformation Matrices]
date created: Friday, September 16th 2022, 9:51:50 am
date modified: Sunday, August 23rd 2026, 11:56:55 am
---

# Transformation Matrix

## Unique Representation of Mapping

Consider [[Vector Space|vector spaces]] $V, W$ with corresponding [[Basis#Ordered Basis|ordered bases]] $B, C$. Moreover, we consider a [[Linear Mapping]] $\Phi: V \rightarrow W$. For $j \in \{ 1, \ldots, n \}$, the following is a unique representation of $\Phi(b_j)$ with respect to $C$.

$$
\Phi(b_j) =
\sum_{i=1}^m a_{ij} c_i
$$

## Definition

The following [[Matrix|matrix]] defined below is the [[Transformation Matrix]] of $\Phi$ (with respect to the [[Ordered Basis]] $B$ of $V$ and $C$ of $W$).

$$
A_{\Phi}(i, j) = \alpha_{ij}
$$

If $\hat{x}$ is the coordinate [[Vector Space|Vector]] of $x \in V$ with respect to $B$ and $\hat{y}$ is the coordinate vector of $y = \Phi(x) \in W$ with respect to $C$, then the following can be used to map coordinates with respect to the [[Ordered Basis]] in $V$ to coordinates with respect to an ordered basis in $W$

$$
\hat{y} = A_{\Phi} \hat{x}
$$

### Example

Consider a [[Homomorphism#Homomorphism|homomorphism]] $a\Phi: V \rightarrow W$ with [[Ordered Basis]] $B = (b_1, \ldots, b_3)$ of $V$ and $C = (c_1, \ldots, c_4)$ of $W$ with the following:

$$
\begin{align}\
\Phi(b_1) &=
	c_1 - c_2 + 3c_3 - c4 \\
\Phi(b_2) &=
	2c_1 + c_2 + 7c_3 + 2c4 \\
\Phi(b_3) &=
	3c_2 + c_3 +4 c4 \\
\end{align}
$$

The [[Transformation Matrix]] $A_{\Phi}$ with respect to $B$ and $C$ satisfies $\Phi(b_k) = \sum_{i = 1}^4 \alpha_{ik} c_i$ for $k = 1, \ldots, 3$ and is given as the following:

$$
A_{\Phi}
=
\begin{bmatrix}
	\alpha_1, \alpha_2, \alpha_3, \alpha_4
\end{bmatrix}
=
\begin{bmatrix}
	 1 & 2 & 0 \\
	-1 & 1 & 3 \\
	 3 & 7 & 1 \\
	-1 & 2 & 4 \\
\end{bmatrix}
$$

## References

1. Mathematics for Machine Learning, Ch.2, pp. 50-58
