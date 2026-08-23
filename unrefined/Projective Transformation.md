---
aliases:
  - Projective Transformations
tags:
  - linear-algebra
date created: Tuesday, October 25th 2022, 4:17:24 pm
date modified: Friday, August 21st 2026, 2:36:27 pm
---

# Projective Transformation

$$
\begin{align}
pH &= p' \\
\begin{bmatrix}
h_{11} & h_{12} & h_{13} \\
h_{21} & h_{22} & h_{23} \\
h_{31} & h_{32} & h_{33} \\
\end{bmatrix}
\begin{bmatrix}
x \\ y \\ 1 \\
\end{bmatrix}
&=
\begin{bmatrix}
x' \\ y' \\ 1 \\
\end{bmatrix}
\end{align}
$$

$$
\begin{align}
&
\begin{cases}
x' &= h_{11} x + h_{12} y + h_{13} \\
y' &= h_{21} x + h_{22} y + h_{23} \\
1 &= h_{31} x + h_{32} y + h_{33} \\
\end{cases}
\\ &
\begin{cases}
x' &= \dfrac
{ h_{11} x + h_{12} y + h_{13} }
{ h_{31} x + h_{32} y + h_{33} } \\
y' &= \dfrac
{ h_{21} x + h_{22} y + h_{23} }
{ h_{31} x + h_{32} y + h_{33} } \\
\end{cases}
\\ &
\begin{cases}
0 &=
{ h_{11} x + h_{12} y + h_{13} }
{ -h_{31} x x' - h_{32} y x' - h_{33} x' } \\
0 &=
{ h_{21} x + h_{22} y + h_{23} }
{ -h_{31} x y' - h_{32} y y' - h_{33} y' } \\
\end{cases}
\end{align}
$$

$$
\begin{bmatrix}
x_{1} & y_{1} & 1 & 0&0&0 & -x_{1}x_{1}' & -y_{1}x_{1}' & -x_{1}' \\
0&0&0 & x_{1} & y_{1} & 1 & -x_{1}y_{1}' & -y_{1}y_{1}' & -y_{1}' \\
x_{2} & y_{2} & 1 & 0&0&0 & -x_{2}x_{2}' & -y_{2}x_{2}' & -x_{2}' \\
0&0&0 & x_{2} & y_{2} & 1 & -x_{2}y_{2}' & -y_{2}y_{2}' & -y_{2}' \\
x_{3} & y_{3} & 1 & 0&0&0 & -x_{3}x_{3}' & -y_{3}x_{3}' & -x_{3}' \\
0&0&0 & x_{3} & y_{3} & 1 & -x_{3}y_{3}' & -y_{3}y_{3}' & -y_{3}' \\
x_{4} & y_{4} & 1 & 0&0&0 & -x_{4}x_{4}' & -y_{4}x_{4}' & -x_{4}' \\
0&0&0 & x_{4} & y_{4} & 1 & -x_{4}y_{4}' & -y_{4}y_{4}' & -y_{4}' \\
\end{bmatrix}
\begin{bmatrix}
 h_{11} \\ h_{12} \\ h_{13} \\
 h_{21} \\ h_{22} \\ h_{23} \\
 h_{31} \\ h_{32} \\ h_{33} \\
\end{bmatrix}
=
\begin{bmatrix}
 0 \\ 0 \\ 0 \\
 0 \\ 0 \\ 0 \\
 0 \\ 0 \\ 0 \\
\end{bmatrix}
$$

$$
\begin{align}
Ah &= 0 \\
A^{\top}Ah &= 0 \\
(U D U^{\top})h &= 0
\end{align}
$$
