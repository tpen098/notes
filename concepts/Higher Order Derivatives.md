---
aliases: [Higher Order Derivative]
tags: [calculus]
date created: Monday, October 24th 2022, 6:29:24 pm
date modified: Thursday, August 20th 2026, 7:14:03 pm
---

# Higher Order Derivatives

## Definition

[[Derivative|Derivatives]] or [[Partial Derivative|Partial Derivatives]] may be applied repeatedly or in cascade as long as the [[Function]] is _differentiable_

$$
\frac{ \partial^n f}{ \partial x_n^{a_{n}} \partial x_{n-1}^{a_{n-1}} \dots \partial x_{1}^{a_{1}} }
:=
\frac{ \partial }{ \partial x_{n} }
\overset{a_{n}}{\dots}
\frac{ \partial }{ \partial x_{n} }
\frac{ \partial }{ \partial x_{n-1} }
\overset{a_{n-1}}{\dots}
\frac{ \partial }{ \partial x_{n-1} }
\dots
\frac{ \partial }{ \partial x_{1} }
\overset{a_{1}}{\dots}
\frac{ \partial }{ \partial x_{1} }
f
$$

## References

1. Mathematics for Machine Learning, pp. 164 - 165
