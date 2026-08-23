---
aliases: [Basis Changes]
tags: [linear-algebra]
date created: Wednesday, October 19th 2022, 3:00:33 pm
date modified: Thursday, August 20th 2026, 6:15:58 pm
---

# Basis Change

## Context

Consider two [[Ordered Basis]] of $V$: $B = (b_1, \ldots, b_n), \tilde{B} = (\tilde{b_1}, \ldots, \tilde{b_n})$, and two [[Ordered Basis]] of $W$: $C = (c_1, \ldots, c_m), \tilde{C} = (\tilde{c_1}, \ldots, \tilde{c_m})$.

Moreover, $A_{\phi} \in \mathbb{R}^{(m \times n)}$ is the [[Transformation Matrix]] of the [[Linear Mapping]] $\Phi: V \rightarrow W$ with respect to the [[Basis]] $B$ and $C$, $\tilde{A_{\phi}} \in \mathbb{R}^{(m \times n)}$ is the corresponding [[Transformation Matrix]] with respect to the [[Basis]] $\tilde{B}$ and $\tilde{C}$ and is given by the following:

$$
\tilde{A_{\Phi}} = T^{-1}A_{\Phi}S
$$

Where $S \in \mathbb{R}^{(n \times n)}$ is the [[Transformation Matrix]] of $id_V$ that maps coordinates with respect to $\tilde{B}$ onto coordinates with respect to $B$, and $T \in \mathbb{R}^{(m \times m)}$ is the [[Transformation Matrix]] of $id_W$ that maps coordinates with respect to $\tilde{C}$ onto coordinates with respect to $C$.

> [!note]
> $\Psi_{B \tilde{B}} = id_V$ and $\Xi_{C \tilde{C} }= id_W$ are identity mappings that map [[Vector Space|Vectors]] onto themselves, but with respect to a different [[Basis|Bases]].

## Summary

$$
\begin{CD}
	V @>\Phi>> W
\end{CD}
$$

$$
\begin{CD}
	B @> \Phi_{CB} >A_{\Phi} > C\\
	@A \Psi_{B \tilde{B}} A S A
	@A T A \Xi_{C\tilde{C}} A\\
	\tilde{B} @>\tilde{A_{\Phi}} > \Phi_{\tilde{C}\tilde{B}} > \tilde{C}
\end{CD}
$$

## References

1. Mathematics for Machine Learning, Ch.2, pp. 50-58
