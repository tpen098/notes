---
tags: [linear-algebra]
aliases: [Orthogonal Matrices]
date created: Tuesday, September 20th 2022, 7:04:25 pm
date modified: Friday, August 21st 2026, 2:20:19 pm
---

# Orthogonal Matrix

## Condition

A [[Square Matrix]] is an [[Orthogonal Matrix]] if and only if its columns are [[Orthonormal]]

$$
A A^{\top} = I = A^{\top} A
$$

## Implications for Inverse

The [[Matrix Inverse]] of an [[Orthogonal Matrix]] is equal to its [[Matrix Transpose]]

$$
	A^{-1} = A^{\top}
$$

## Length Invariance

Using the [[Dot Product]], the [[Norm|Length]] of a [[Vector Space|Vector]] $x$ is not changed when [[Transformation Matrix|transformed]] using an [[Orthogonal Matrix]] $A$.

$$
\lVert A x\rVert^2
=
(Ax)^{\top}(Ax)
=
x^{\top}A^{\top}Ax
=
x^{\top}Ix
=
\lVert x\rVert^2
$$

## Angle Invariance

Using the [[Dot Product]], the [[Angle]] between [[Vector Space|Vectors]], $x, y$, is not changed when both are transformed with [[Orthogonal Matrix]] $A$.

$$
\begin{align}
\cos{\omega}
&=
\dfrac{(A x)^{\top} (Ay)}
	  {\lVert A x\rVert \lVert A y\rVert}
\\
&=
\dfrac{x^{\top} A^{\top} A y}
	  {\sqrt{
	  x^{\top} A^{\top} A x
	  y^{\top} A^{\top} A y}}
\\
&=
\dfrac{x^{\top} y}
	  {\lVert x\rVert \lVert y\rVert}
\end{align}
$$

## References

1. Mathematics for Machine Learning, Ch.3, p. 78
