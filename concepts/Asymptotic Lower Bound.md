---
aliases:
  - Asymptotic Lower Bounds
  - Best-Case
  - Best-Case Complexity
tags:
  - optimization
date created: Thursday, March 14th 2024, 1:41:14 pm
date modified: Sunday, August 16th 2026, 3:55:08 pm
---

# Asymptotic Lower Bound

## Definition

The [[Asymptotic Lower Bound]] $\Omega$-notation is the [[Function]] $\Omega(\cdot)$ that takes a [[Function]] $g(n)$ to produce the [[Set]] of [[Function|Functions]] $\Omega(g(n))$ containing [[Function|Functions]] $f(n)$ such that $c g(n) \leq f(n)$ for sufficiently large $n$ [^1]

$$
\forall n \geq n_{0}, \Omega(g(n)) = \{ 0 \leq c g(n) \leq f(n) \}
$$

## Intuition

Consider a [[Function]] that describes a running time for an [[Algorithm]] $r(n)$. The lower bound of the running time $r(n)$ as $n$ is at least $c n^2$ because there exists a constant $c$ such that $r(n) \geq c n^2$. To formally describe this, the following expression is used

$$
r(n) \in \Omega(n^2)
$$

However, the notation often uses [[Set Equality]] [^1]

$$
r(n) = \Omega(n^2)
$$

> [!info]
> By definition, the [[Asymptotic Lower Bound]] also covers for excessively smaller $g(n)$. For example, if a running time $r(n) \in \Omega(n^{3})$ then it is also $r(n) \in O(n^{2}), O(n^{1}), \dots$

For a formal example, consider a running time $r(n) = 4 n^{2} + 100 n + 500$ with $g(n) = cn^{2}$

$$
\begin{align}
r(n) & \geq c n^{2} \\
4 n^{2} + 100 n + 400 &\geq c n^2 \\
4 + \frac{100}{n} + \frac{400}{n^{2}} &\geq c \\
\lim_{ n \to \infty } 4 + \frac{100}{n} + \frac{400}{n^{2}} &\geq \lim_{ n \to \infty } c \\
4  \geq c
\end{align}
$$

Given that the required constant $c$ is viable for the definition, $r(n) \in \Omega(g(n))$

## Properties

### Transitivity Property

The [[Function|Argument]] of an [[Asymptotic Lower Bound]] that is an [[Function|Argument]] of another [[Asymptotic Lower Bound]] can be simplified to just the an [[Asymptotic Lower Bound]] with the innermost [[Function|Argument]] as shown [^2]

$$
f(n) = \Omega(g(n)), g(n) = \Omega(h(n)) \implies f(n) = \Omega(h(n))
$$

### Reflexivity Property

A given [[Function]] $f(n)$ is equal to its [[Asymptotic Lower Bound]] $\Omega(f(n))$ [^2]

$$
f(n) = \Omega(f(n))
$$

### Symmetry Property

Applying the [[#Reflexivity Property]] and [[#Transitivity Property]] results to the assertion that a [[Function]] $f(n)$ is equal to a [[Asymptotic Lower Bound]] $\Theta(g(n))$ if and only if $g(n) = \Omega(f(n))$ [^2]

$$
f(n) = \Omega(g(n)) \iff g(n) = \Omega(f(n))
$$

## References

[1]: Introduction to Algorithms, pp. 51, 55-56

[2]: Introduction to Algorithms, pp. 61-62
