---
tags:
  - linear-algebra
aliases:
  - Matrix Gradient Identity
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Friday, August 21st 2026, 1:25:33 pm
---

# Matrix Gradient Identities

## Transpose of a Matrix Gradient

$$
\frac{ \partial }{ \partial X } f(X)^{\top}
= \left( \frac{ \partial }{ \partial X } f(X) \right)^{\top}
$$

## Trace of a Matrix Gradient

$$
\frac{ \partial }{ \partial X } tr(f(X))
= tr \left( \frac{ \partial }{ \partial X } f(X)\right)
$$

## Gradient of a Matrix Determinant

$$
\frac{ \partial }{ \partial X } \det(f(X))
= \det(f(X)) tr(f(X)^{-1} \frac{ \partial }{ \partial X } f(X))
$$

## Gradient of a Matrix Inverse

$$
\frac{ \partial }{ \partial X } f(X)^{-1}
= - f(X)^{-1} \frac{ \partial }{ \partial X } f(X) f(X)^{-1}
$$

## Gradient of a Dot Product

$$
\frac{ \partial }{ \partial x} x^{\top} a =
\frac{ \partial }{ \partial x} a^{\top} x =
a^{\top}
$$

$$
\frac{ \partial }{ \partial X } a^{\top} Xb = ab^{\top}
$$

$$
\frac{ \partial }{ \partial x } x^{\top} Bx =
x^{\top} (B + B^{\top})
$$

## References

1. Mathematics for Machine Learning, pp. 158-159
