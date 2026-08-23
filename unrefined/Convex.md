---
aliases:
  - Jensen’s Inequality
tags:
  - linear-algebra
date created: Tuesday, November 15th 2022, 3:11:21 pm
date modified: Friday, August 21st 2026, 3:45:32 pm
---

# Convex

## Definition

Given a real-valued [[Function]] $f: \mathbb{R}^D \to \mathbb{R}$ whose [[Domain]] is in a [[Convex Set]], the [[Function]] is [[Convex]] if $\forall x, y$ in the [[Domain]] of $f$, and for any scalar $0 \leq \theta \leq 1$, the following condition holds

$$
f(\theta x + (1 + \theta)y) \leq
\theta f(x) + (1+\theta)f(x)
$$

Alternatively, the [[Function]] $f$ is [[Convex]] if and only if for two points $x,y$ the following condition holds

$$
f(y) \leq f(x) + \nabla_{x}f(x)^{\top} (y-x)
$$

> [!NOTE] Positive-Semidefiniteness
> If the [[Hessian Matrix]], $A = \nabla_{x}^2 f$ exists, then it is positive, semidefinite
>
> $$\forall x \in V: x^{\top}Ax \geq 0$$
