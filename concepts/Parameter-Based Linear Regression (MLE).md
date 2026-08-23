---
aliases: [MLE, Parameter-Based Linear Regressions]
tags: [statistics-probability, machine-learning]
date created: Saturday, November 26th 2022, 12:57:11 pm
date modified: Friday, August 21st 2026, 2:26:21 pm
---

# Parameter-Based Linear Regression (MLE)

## Loss Function Derivation

Given a [[Parameter-Based Linear Regression|Parameter-Based Linear Regression Problem]] with [[Dataset]] $\mathcal{D}$ and [[Independent and Identically Distributed|IID]] [[Gaussian Distribution|Normal Distribution]] noise $\epsilon \sim \mathcal{N}(0, \sigma^2)$, the [[Maximum Likelihood Estimation]] can be seen as a [[Loss Function]] $\mathcal{L}(\theta)$ to be minimized. The constant $C$ in the derivation is often ignored.

$$
\begin{align}
\mathcal{L}(\theta)
&= -\log(p(\mathcal{Y}|\mathcal{X},\theta)) \\
&= -\log\left( \prod_{n=1}^{N} p(y_{n}|\phi ^{\top}(x_{n}), \theta) \right) \\
&= - \sum_{n=1}^{N} \log(p(y_{n}| \phi ^{\top}(x_{n}), \theta)) \\
&= - \frac{1}{2\sigma^2} \sum_{n=1}^{N} (y_{n}-\phi ^{\top}(x_{n})\theta)^2 + C_{n} \\
&= \frac{1}{2\sigma^2}
(y -\Phi \theta)^{\top}(y - \Phi\theta) + C \\
&= \frac{1}{2\sigma^2}
\lVert y - \Phi \theta \rVert^2 + C
\end{align}
$$

## Loss Function Minimization

If parameter $\theta_{ML}$ optimizes the [[Machine Learning Model|Model]], the [[Partial Derivative|Gradient]] of the [[Loss Function]] must be the zero vector. This can be determined using the [[Matrix Gradient Identities]]

$$
\begin{align}
\frac{ d\mathcal{L} }{ d\theta }
&= \frac{ d }{ d\theta } \left( \frac{1}{2\sigma^2}
(y-\Phi\theta)^{\top}(y-\Phi\theta) \right) \\
&= \frac{1}{2\sigma^2} \frac{ d }{ d\theta }
( y^{\top}y
- 2 y^{\top} \Phi \theta
+ \theta^{\top} \Phi^{\top} \Phi \theta) \\
&= \frac{1}{\sigma^2} (-y^{\top} \Phi + \theta ^{\top} \Phi ^{\top}\Phi)
\in \mathbb{R}^{1 \times K}
\end{align}
$$

The condition for optimization to globally optimize the parameter $\theta_{{ML}}$

$$
\begin{align}
0^{\top}
&= \frac{1}{\sigma^2}
(-y^{\top} \Phi + \theta ^{\top}_{ML} \Phi ^{\top}\Phi) \\
\theta_{ML} ^{\top} \Phi ^{\top}\Phi
&= y^{\top}\Phi \\
\theta_{ML}^{\top}
&= y^{\top}\Phi(\Phi^{\top}\Phi)^{-1} \\
\theta_{ML}
&= (\Phi^{\top}\Phi)^{-1} \Phi^{\top} y \\
\end{align}
$$

> [!NOTE] Reinterpretation as a System of Linear Equations
> The problem is a [[Linear System]] with weight $A = \Phi^{\top}\Phi$ and bias $b=\Phi^{\top}y$
>
>$$\begin{align}
> \theta_{ML} ^{\top} \Phi ^{\top}\Phi &= y^{\top}\Phi \\
> A \theta_{ML} &= b \end{align}$$

## Noise Variance Derivation

Assuming the [[Variance]] $\sigma^2$ is not known for a [[Gaussian Distribution|Normal Distribution]] noise, the [[Maximum Likelihood Estimation]] can also be used to estimate it as shown

$$
\begin{align}
\log(p(\mathcal{Y}|\mathcal{X}, \theta, \sigma^2))
&= \sum_{n=1}^{N} \left(
- \frac{1}{2} \log(2\pi) - \frac{1}{2} \log(\sigma^2)
- \frac{1}{2\sigma^2} (y_{n}-\phi ^{\top}(x_{n})\theta)^2 \right)\\
&= -\frac{N}{2}\log(\sigma^2)
- \frac{1}{2\sigma^2} \sum_{n=1}^{N} (y_{n} - \phi ^{\top}(x_{n})\theta) + C
\end{align}
$$

For optimization, the [[Partial Derivative]] of the [[Maximum Likelihood Estimation|Log]] [[Bayes' Theorem|Likelihood Function]] must be zero with respect to the [[Variance]] $\sigma^2$. This results to the normalized [[Least Squares Error]]

$$
\begin{align}
\dfrac{\partial}{\partial \sigma^2}
\log(p(\mathcal{Y}|\mathcal{X}, \theta, \sigma^2))
&= -\frac{N}{2\sigma^2}+\frac{1}{2\sigma^4}
\lVert y - \Phi \theta \rVert^2 = 0 \\
\sigma^2_{{}} &= \frac{1}{N} \lVert y - \Phi \theta \rVert^2 = 0
\end{align}
$$

## Root Mean Squared Loss Function

The [[Root Mean Squared Error]] is usually used for [[Loss Function|Loss]] as it allows for comparison between [[Dataset|Datasets]] with different $N$ and the [[Loss Function|Loss]] output has the same scale and unit as the output $y$. With the existing [[Loss Function]], the scaling factor $\sigma^{-2}$ is replaced with $N^{-1}$ and a square root is applied to convert the [[Least Squares Error|L2 Loss]] to [[Root Mean Squared Error|RMSE]] form.

$$
\sqrt{ \frac{1}{N} \lVert y - \Phi\theta \rVert^2 }
= \sqrt{ \frac{1}{N} \sum_{n=1}^N (y_{n}-\phi ^{\top}(x_{n})\theta)^2 }
$$

## References

1. Mathematics for Machine Learning, pp. 292-300
