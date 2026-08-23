---
tags: [machine-learning]
aliases: [Deep Neural Networks]
date created: Monday, September 12th 2022, 3:27:48 pm
date modified: Sunday, August 16th 2026, 11:28:42 pm
---

# Deep Neural Network

## Mathematical Model

A [[Deep Neural Network]] can be modelled as a series of convolutions as shown

$$
\begin{align}
y &= (f_k \circ f_{K-1} \circ \dots \circ f_{1})(x) \\
{}&= f_{K}(f_{K-1}(\dots(f(k))\dots))
\end{align}
$$

![[Deep Neural Network.png]]

## Layer Parameters

Each [[Function]] $f_i$ in the $i$-th layer of the [[Deep Neural Network]] is recursively defined as the past output $f_{i-1}$ scaled by a _weight_ parameter $A_{i-1}$ and offset by a _bias_ parameter $b_{i-1}$ being fed into an [[Activation Function]] $\sigma(\cdot)$ as shown in the following

$$
\begin{align}
f_{0} &:= x \\
f_{i}(x_{i-1}) &:= \sigma(A_{i-1} f_{i-1} + b_{i-1}) \\
\end{align}
$$

## References

1. Mathematics for Machine Learning, pp.159-165
