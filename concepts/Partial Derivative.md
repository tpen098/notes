---
tags:
  - calculus
aliases:
  - Partial Derivatives
  - Gradient
  - Gradients
  - Jacobian
  - Jacobians
date created: Thursday, October 20th 2022, 5:51:46 pm
date modified: Sunday, August 23rd 2026, 11:54:27 am
---

# Partial Derivative

## General Definition

Given the following definition of a general vector-valued [[Function]]

$$
f: \mathbb{R}^n \to \mathbb{R}^m \atop
x \mapsto f(x),
x = [x_{1}, \dots, x_{n}]^{\top} \in \mathbb{R}^n
$$

$$
f(x) = \begin{bmatrix}
f_{1}(x) \\
\dots \\
f_{m}(x)
\end{bmatrix}
\in \mathbb{R}^m
$$

The [[Partial Derivative]] of [[Function]] $f$ with respect to $x_i$ is defined as the following

$$
\frac{ \partial f }{ \partial x_{i} }
= \begin{bmatrix}
\frac{ \partial f_{1} }{ \partial x_{i} } \\
\vdots \\
\frac{ \partial f_{m} }{ \partial x_{i} } \\
\end{bmatrix}
= \begin{bmatrix}
\lim_{ h_ \to 0 } \frac{f_{1}(x_{1},\dots,x_{i-1},x_{i}+h,x_{i+1},\dots,x_{n}) - f_{1}(x)}{h} \\
\vdots \\

\lim_{ h_ \to 0 } \frac{f_{1}(x_{1},\dots,x_{i-1},x_{i}+h,x_{i+1},\dots,x_{n}) - f_{m}(x)}{h} \\
\end{bmatrix}
$$

### Jacobian

The [[Partial Derivative|Partial Derivatives]] of every $f_{i}$ for every $x_i \in x$ can be collected into a [[Matrix]] as the [[Partial Derivative|Gradient]] of $f$ or [[Partial Derivative|Jacobian]] as shown in the following

$$
J = \nabla_{x}f=
\frac{ df(x) }{ dx }
= \begin{bmatrix}
\frac{ \partial f_{1}(x) }{ \partial x } \\
\vdots \\
\frac{ \partial f_{m}(x) }{ \partial x } \\
\end{bmatrix}
= \begin{bmatrix}
\frac{ \partial f_{1}(x) }{ \partial x_{1} } & \dots & \frac{ \partial f_{1}(x) }{ \partial x_{n} }\\
\vdots & & \vdots\\
\frac{ \partial f_{m}(x) }{ \partial x_{1} } & \dots & \frac{ \partial f_{m}(x) }{ \partial x_{n} }\\
\end{bmatrix}
$$

> [!caution] Function with multiple inputs but singular output
> For the special case wherein there is only one $f_i$, the [[Jacobian]] simplifies to the following row vector.
>
>$$
> 
>\nabla_{x}f
>= \frac{ df }{ dx }
>= \begin{bmatrix}
>\frac{ \partial f(x) }{ \partial x_{1} } &
>\frac{ \partial f(x) }{ \partial x_{1} } &
>\dots &
>\frac{ \partial f(x) }{ \partial x_{n} } &
>\end{bmatrix} \in \mathbb{R}^{1 \times n}
>
>$$

## Layout

The layout established is called the _numerator layout_. The transpose of the current layout is the _Denominator Layout_.

> [!NOTE] Function with multiple inputs but singular output
> If the Jacobian is $1 \times n$ in _numerator layout_, then it becomes a column vector $n \times 1$ in _denominator layout_,

## References

1. Mathematics for Machine Learning, Ch. 5, p. 146-151
