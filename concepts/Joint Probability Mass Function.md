---
aliases: [Joint Probability, Discrete Joint Probability]
tags: [statistics-probability]
date created: Tuesday, November 1st 2022, 12:36:56 pm
date modified: Sunday, August 23rd 2026, 11:53:44 am
---

# Joint Probability Mass Function

## Definition

Given [[Random Variable|Random Variables]] $X_{1}, X_{2}, \dots, X_{n}$ of a discrete [[Target Space]], the Joint [[Probability Mass Function]] is defined as the following:

$$
\begin{align}
p(x_{i_{1}}, \dots, x_{i_{n}})
&= P(X_{1}=x_{i_{1}}, \dots, X_{n}=x_{i_{n}}) \\
&= P(X_{1}=x_{i_{1}} \cap \dots \cap X_{n}=x_{i_{n}})
\end{align}
$$

Where $n_{(i_{1}\dots i_{n})}$ is the number of events with states with $x_{i_{1}}, \dots, _{i_{n}}$ simultaneously, and $N$ is the total number of events.

## Two-Dimensional Example

Given [[Random Variable|Random Variables]] $X, Y$, the [[Joint Probability Mass Function|Joint Probability]] $P(X=x_{i}, Y=y_{j})$ is given as the cell that intersects $x_i$ and $y_j$.

$$
P(X=x_{i}, Y=y_{j}) 
= \frac{\sum p_{(i, j)}}{\sum p}
$$

$$
\begin{matrix}
x_{1} \\ x_{2} \\ \vdots \\ x_{m} \\
\end{matrix}
\begin{array}{| c | c | c | }
\hline
p_{11} & p_{12} & \dots & p_{1n}\\
\hline
p_{21} & p_{22} & \dots & p_{2n} \\
\hline
\vdots & \vdots & \ddots & \vdots \\
\hline
p_{m_{1}} & p_{m_{2}} & \dots & p_{mn} \\
\hline
\end{array}
\atop
\begin{matrix}
y_{1} & y_{2} & \;\;\;\; \dots & y_{n} \\
\end{matrix}
$$

## References

1. Mathematics for Machine Learning, pp. 177-178
