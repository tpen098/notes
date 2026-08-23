---
aliases: [Hessian Matrices]
tags: [linear-algebra, calculus]
date created: Sunday, August 16th 2026, 1:18:43 pm
date modified: Thursday, August 20th 2026, 7:13:27 pm
---

# Hessian Matrix

## Definition

The [[Hessian Matrix]] $\nabla^2_{x_{1}, x_{2}, \dots, x_{n}} f(x_{1}, x_{2}, \dots, x_{n})$ is defined as the collection of all second-order, [[Higher Order Derivatives]] of the [[Function]] $f$ with respect to [[Variable|Variables]] $x_1, \dots, x_n$, represented using a [[Symmetric Matrix|Symmetric]] [[Square Matrix]] as shown

$$
\begin{bmatrix}
\frac{ \partial^2 f }{ \partial x_{1} \partial x_{1} }  &
\frac{ \partial^2 f }{ \partial x_{1} \partial x_{2} }  & 
\dots &
\frac{ \partial^2 f }{ \partial x_{1} \partial x_{n} } \\  \\
\frac{ \partial^2 f }{ \partial x_{2} \partial x_{1} }  &
\frac{ \partial^2 f }{ \partial x_{2} \partial x_{2} }  & 
\dots &
\frac{ \partial^2 f }{ \partial x_{2} \partial x_{n} } \\  
\vdots & \vdots & \ddots & \vdots \\ \\
\frac{ \partial^2 f }{ \partial x_{n} \partial x_{1} }  &
\frac{ \partial^2 f }{ \partial x_{n} \partial x_{2} }  & 
\dots &
\frac{ \partial^2 f }{ \partial x_{n} \partial x_{n} } \\ 
\end{bmatrix}
$$

## References

1. Mathematics for Machine Learning, p. 165
