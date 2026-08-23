---
aliases: [Gradient Descent]
tags: [machine-learning, optimization]
date created: Monday, October 24th 2022, 2:23:40 pm
date modified: Friday, August 21st 2026, 3:45:08 pm
---

# Backpropagation

## Motivation

To optimize a [[Function]] with parameter $\theta \in \mathbb{R}^K$, the [[Partial Derivative]] of the [[Loss Function]] $L(\theta)$ must be zero with respect to every layer or parameter with the form $\theta_{i} = A_{i-1}f_{i-1}+b_{i-1}$ with scaling weight $A_{i}$ and additive bias $b_{i}$.

$$
\frac{ dL(\theta) }{ d\theta } = 0
$$

## Inner and Outer Partial Derivatives

Through the repeated use of the [[Chain Rule]], the [[Partial Derivative|Partial Derivatives]] of the layer functions with respect to their inputs $\frac{ \partial f_{i} }{ \partial f_{i-1} }$ and with respect to their parameters $\frac{ \partial f_{i+1} }{ \partial \theta_{i} }$ for the [[Partial Derivative|Partial Derivatives]] of the [[Loss Function]] $L$.

$$
\begin{align}
\frac{ \partial L }{ \partial \theta_{K-1} } &=
\frac{ \partial L }{ \partial f_{K} }
\frac{ \partial f_{K} }{ \partial \theta_{K-1} } \\
\frac{ \partial L }{ \partial \theta_{K-2} } &=
\frac{ \partial L }{ \partial f_{K} }
\frac{ \partial f_{K} }{ \partial \theta_{K-1} }
\frac{ \partial f_{K-1} }{ \partial \theta_{K-2} } \\
\frac{ \partial L }{ \partial \theta_{K-3} } &=
\frac{ \partial L }{ \partial f_{K} }
\frac{ \partial f_{K} }{ \partial \theta_{K-1} }
\frac{ \partial f_{K-1} }{ \partial \theta_{K-2} }
\frac{ \partial f_{K-2} }{ \partial \theta_{K-3} } \\
&\vdots \\
\frac{ \partial L }{ \partial \theta_{i} } &=
\frac{ \partial L }{ \partial f_{K} }
\frac{ \partial f_{K} }{ \partial \theta_{K-1} }
\dots
\frac{ \partial f_{i+2} }{ \partial \theta_{i+1} }
\frac{ \partial f_{i+1} }{ \partial \theta_{i} }
\end{align}
$$

The method generalizes to the following

$$
\frac{ \partial L }{ \partial \theta_{i} } =
\frac{ \partial L }{ \partial f_{K} }
\frac{ \partial f_{K} }{ \partial \theta_{K-1} }
\dots
\frac{ \partial f_{i+2} }{ \partial \theta_{i+1} }
\frac{ \partial f_{i+1} }{ \partial \theta_{i} }
$$

> [!tip] Recursive Definition
> For layers before the $K-1$ last layer, the computation of the [[Partial Derivative|Partial Derivatives]] can be simplified by using the proceeding layer and simply multiplying it with the $\frac{ \partial f_{i+1} }{ \partial \theta_{i} }$ term.

## Parameter-Based Partial Derivatives

The [[Partial Derivative]] of the [[Loss Function]] with respect to a layer $i$ can be obtained using $\theta$ as the dependency as shown in the following

$$
\frac{ \partial L }{ \partial \theta_{i} } =
\frac{ \partial L }{ \partial \theta_{K-1} }
\frac{ \partial \theta_{K-1} }{ \partial \theta_{K-2} }
\dots
\frac{ \partial \theta_{i+2} }{ \partial \theta_{i+1} }
\frac{ \partial \theta_{i+1} }{ \partial \theta_{i} }
$$

Parameter-by-parameter [[Partial Derivative|Partial Derivatives]] can be rewritten into a product of two [[Partial Derivative|Partial Derivatives]] with $f_i$ as the dependency.

$$
\frac{ \partial \theta_{i+1} }{ \partial \theta_{i} } =
\frac{ \partial \theta_{i+1} }{ \partial \theta_{i} }(1) =
\frac{ \partial \theta_{i+1} }{ \partial \theta_{i} }
\frac{ \partial f_{i} }{ \partial f_{i} } =
\frac{ \partial \theta_{i+1} }{ \partial f{i} }
\frac{ \partial f_{i} }{ \partial \theta_{i} }
$$

The alternative, general solution to the [[Partial Derivative]] of the [[Loss Function]] is defined as the following

$$
\frac{ \partial L }{ \partial \theta_{i} } =
\frac{ \partial L }{ \partial \theta_{K-1} }
\frac{ \partial \theta_{K-1} }{ \partial f_{K-2} }
\frac{ \partial f_{K-2} }{ \partial \theta_{K-2} }
\frac{ \partial \theta_{K-2} }{ \partial f_{K-2} }
\frac{ \partial f_{K-2} }{ \partial \theta_{K-3} }
\dots
\frac{ \partial \theta_{i+1} }{ \partial f_{i} }
\frac{ \partial f_{i} }{ \partial \theta_{i} }
$$

> [!tip] Recursive Definition
> For layers before the $K-1$ last layer, the computation of the [[Partial Derivative|Partial Derivatives]] can also be simplified with this technique by using the proceeding layer and simply multiplying it with the $\frac{ \partial f_{i} }{ \partial \theta_{i} }$ term.

## Layer Parameters

The weight $A_{i-1}$ and _bias_ $b_{i-1}$ parameters can be solved by using the [[Chain Rule]] with the $\theta_{i}$ as the dependency variable.

$$
\begin{align}
\frac{ \partial L }{ \partial A_{n-1} }
&=
\frac{ \partial L }{ \partial \theta_{i} }
\frac{ \partial \theta_{i} }{ \partial A_{i-1} }
=
\frac{ \partial L }{ \partial \theta_{i} }
\frac{ \partial (A_{i-1}f_{i-1}+b_{i-1}) }{ \partial A_{i-1} }
=
\frac{ \partial L }{ \partial \theta_{i} } (f_{i-1}) \\
\\
\frac{ \partial L }{ \partial b_{i-1} }
&=
\frac{ \partial L }{ \partial \theta_{i} }
\frac{ \partial \theta_{i} }{ \partial b_{i-1} }
=
\frac{ \partial L }{ \partial \theta_{i} }
\frac{ \partial (A_{i-1}f_{i-1}+b_{i-1}) }{ \partial b_{i-1} }
=
\frac{ \partial L }{ \partial \theta_{i} } (1) \\
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp.159-165
