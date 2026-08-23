---
aliases:
  - Bases
tags:
  - linear-algebra
date created: Thursday, September 15th 2022, 10:12:28 pm
date modified: Tuesday, August 18th 2026, 9:16:03 pm
---

# Basis

## Definition

Every minimal, [[Linear Independence|Linearly Independent]] [[Generating Set]] of $V$ is called a [[Basis]] of $V$. Every [[Vector Space|Vector]] of $V$ is a [[Linear Combination]] of [[Vector Space|Vectors]] from the [[Generating Set]] and every [[Linear Combination]] is unique.

> [!NOTE] Non-unique Property
> Every [[Vector Space]] posses a [[Basis]] and there is no unique [[Basis]]. However, all [[Basis]] have the same number of [[Set Membership|Elements]].

## Procedure to Find the Basis of a Subspace

1. Write the spanning [[Vector Space|Vectors]] as columns of a new [[Matrix]]
2. Determine the [[Matrix Row Echelon Form]]
3. The [[Span|Spanning]] [[Vector Space|Vectors]] associated with the pivot column are the [[Basis]]

### Example

For a [[Vector Subspace]] $U \subseteq \mathbb{R}^5$ spanned by the [[Vector Space|Vectors]]:

$$
x_1 =
\begin{bmatrix}
1 \\ 2 \\ - 1 \\ -1 \\ -1 \\
\end{bmatrix},
x_2 =
\begin{bmatrix}
2 \\ -1 \\ 1 \\ 2 \\ -2 \\
\end{bmatrix},
x_3 =
\begin{bmatrix}
3 \\ -4 \\ 3 \\ 5 \\ -3 \\
\end{bmatrix}
x_4 =
\begin{bmatrix}
-1 \\ 8 \\ -5 \\ -6 \\ 1 \\
\end{bmatrix}
$$

The first step would be to convert the spanning columns into a [[Matrix]]

$$
\begin{bmatrix}
x_1 & x_2 & x_3 & x_4 & x_5
\end{bmatrix}
=
\begin{bmatrix}
1 & 2 & 3 & -1 \\
2 & -1 & -4 & 8 \\
-1 & 1 & 3 & -5 \\
-1 & 2 & 5 & -6 \\
-1 & -2 & -3 & 1 \\
\end{bmatrix}
$$

The second step is to convert the [[Matrix]] into [[Matrix Row Echelon Form]]

$$
\begin{bmatrix}
1 & 2 & 3 & -1 \\
2 & -1 & -4 & 8 \\
-1 & 1 & 3 & -5 \\
-1 & 2 & 5 & -6 \\
-1 & -2 & -3 & 1 \\
\end{bmatrix}
\rightarrow
\begin{bmatrix}
1 & 2 & 3 & -1 \\
0 & 1 & 2 & -2 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
\end{bmatrix}
$$

From the resulting [[Matrix]], column [[Vector Space|Vectors]] $x_1, x_2, x_4$ are a [[Basis]] of $U$

## References

1. Mathematics for Machine Learning, ch.2, pp. 44-47, 50-51
