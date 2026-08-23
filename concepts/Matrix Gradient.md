---
aliases: [Matrix Gradients]
tags: [linear-algebra, calculus]
date created: Monday, October 24th 2022, 8:53:46 am
date modified: Friday, August 21st 2026, 1:24:56 pm
---

# Matrix Gradient

## Definition via Projection

Given two [[Matrix|Matrices]] $A \in \mathbb{R}^{m \times n}, B \in \mathbb{R}^{p \times q}$, assumed to be [[Linear Mapping]]

$$
A =
\begin{bmatrix}
	a_{11} & a_{12} & \ldots & a_{1n} \\
	a_{21} & a_{22} & \ldots & a_{2n} \\
	\vdots & \vdots & \ddots & \vdots \\
	a_{m1} & a_{m2} & \ldots & a_{mn}
\end{bmatrix},
B =
\begin{bmatrix}
	b_{11} & b_{12} & \ldots & b_{1q} \\
	b_{21} & b_{22} & \ldots & b_{2q} \\
	\vdots & \vdots & \ddots & \vdots \\
	b_{p1} & b_{p2} & \ldots & b_{pq}
\end{bmatrix}
$$

Using the [[Isomorphism]] between a space $\mathbb{R}^{a \times b}$ and $\mathbb{R}^{a b}$, the [[Matrix|Matrices]] can be reshaped into the following vectors instead

$$
A =
\begin{bmatrix}
	a_{11} \\ \vdots \\ a_{1n} \\ a_{21} \\ \vdots \\ a_{mn}
\end{bmatrix},
B =
\begin{bmatrix}
	b_{11} \\ \vdots \\ b_{1q} \\ b_{21} \\ \vdots \\ b_{pq}
\end{bmatrix} \\
$$

The resulting [[Partial Derivative|Jacobian]] will be the following [[Matrix]]

$$
\frac{ dA }{ dB } =
\begin{bmatrix}
\begin{bmatrix}
	\frac{ \partial a_{11} }{ \partial b_{11} } & \dots &
	\frac{ \partial a_{11} }{ \partial b_{1q} } \\
	\vdots & \ddots & \vdots \\
	\frac{ \partial a_{11} }{ \partial b_{p1} } & \dots &
	\frac{ \partial a_{11} }{ \partial b_{pq} } \\
\end{bmatrix} &
\dots &
\begin{bmatrix}
	\frac{ \partial a_{1n} }{ \partial b_{11} } & \dots &
	\frac{ \partial a_{1n} }{ \partial b_{1q} } \\
	\vdots & \ddots & \vdots \\
	\frac{ \partial a_{1n} }{ \partial b_{p1} } & \dots &
	\frac{ \partial a_{1n} }{ \partial b_{pq} } \\
\end{bmatrix} \\
\vdots & \ddots & \vdots \\
\begin{bmatrix}
	\frac{ \partial a_{m1}}{ \partial b_{11} } & \dots &
	\frac{ \partial a_{m1} }{ \partial b_{1q} } \\
	\vdots & \ddots & \vdots \\
	\frac{ \partial a_{m1} }{ \partial b_{p1} } & \dots &
	\frac{ \partial a_{m1} }{ \partial b_{pq} } \\
\end{bmatrix} &
\dots &
\begin{bmatrix}
	\frac{ \partial a_{mn} }{ \partial b_{11} } & \dots &
	\frac{ \partial a_{mn} }{ \partial b_{1q} } \\
	\vdots & \ddots & \vdots \\
	\frac{ \partial a_{mn} }{ \partial b_{p1} } & \dots &
	\frac{ \partial a_{mn} }{ \partial b_{pq} } \\
\end{bmatrix} \\
\end{bmatrix}
$$

## Definition by Index

For each element $a_{ij} \in A$, an element of the gradient of matrix $A$ with respect to matrix $B$ can be defined as the following

$$
\frac{ \partial A_{ij} }{ \partial B } =
\frac{ \partial a_{ij} }{ \partial B } =
\begin{bmatrix}
	\frac{ \partial a_{ij} }{ \partial b_{11} } & \dots &
	\frac{ \partial a_{ij} }{ \partial b_{1q} } \\
	\vdots & \ddots & \vdots \\
	\frac{ \partial a_{ij} }{ \partial b_{p1} } & \dots &
	\frac{ \partial a_{ij} }{ \partial b_{pq} } \\
\end{bmatrix}
$$

## References

1. Mathematics for Machine Learning, pp. 155-157
