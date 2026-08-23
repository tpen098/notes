---
aliases: []
tags: [machine-learning]
date created: Tuesday, November 15th 2022, 1:44:05 pm
date modified: Friday, August 21st 2026, 3:47:38 pm
---

# Gradient Descent Momentum

## Definition

The [[Gradient Descent]] can add the contribution of the past [[Partial Derivative|Gradients]] by a scaling factor $\alpha$, commonly $\alpha \in [0, 1]$ to the current update for faster convergence. [^1]

$$
\begin{align}
\theta_{{i+1}} &
= \theta_{i} 
- \epsilon_{i} ((\nabla f)(\theta_{i}))^{\top} + \alpha g \\
g &
= \theta_{i} 
- \theta_{i-1} \\
\theta_{{i+1}} &
= \theta_{i} 
- \epsilon_{i} ((\nabla f)(\theta_{i}))^{\top} 
+ \alpha (\theta_{i} 
- \theta_{i-1}) \\
\end{align}
$$

## References

[^1]: Mathematics for Machine Learning, pp. 230-231
