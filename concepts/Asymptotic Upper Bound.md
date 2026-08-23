---
aliases:
  - Asymptotic Upper Bounds
  - Worst-Case
  - Worst-Case Complexity
tags:
  - optimization
date created: Thursday, March 14th 2024, 1:20:43 pm
date modified: Sunday, August 16th 2026, 3:55:16 pm
---

# Asymptotic Upper Bound

## Definition

The [[Asymptotic Upper Bound]] $O$-notation is the [[Function]] $O(\cdot)$ that takes a [[Function]] $g(n)$ to produce the [[Set]] of [[Function|Functions]] $O(g(n))$ containing [[Function|Functions]] $f(n)$ such that $f(n) \leq c g(n)$ for sufficiently large $n$. [^1]

$$
\forall n \geq n_{0}, O(g(n)) =\{ 0 \leq f(n) \leq c g(n) \}
$$

## Intuition

Consider a [[Function]] that describes a running time for an [[Algorithm]] $r(n)$. The upper bound of the running time $r(n)$ as $n$ increases is $c n^2$ because there exists a constant $c$ such that $r(n) \leq c n^2$. To formally describe this, the following expression is used

$$
r(n) \in O(n^2)
$$

However, the notation often uses [[Set Equality]] [^1]

$$
r(n) = O(n^2)
$$

> [!info]
> By definition, the [[Asymptotic Upper Bound]] also covers for excessively larger $g(n)$. For example, if a running time $r(n) \in O(n^{2})$ then it is also $r(n) \in O(n^{3}), O(n^{4}), \dots$

For a formal example, consider a running time $r(n) = 4 n^{2} + 100 n + 500$ with $g(n) = cn^{2}$

$$
\begin{align}
r(n) & \leq c n^{2} \\
4 n^{2} + 100 n + 400 &\leq c n^2 \\
4 + \frac{100}{n} + \frac{400}{n^{2}} &\leq c \\
\lim_{ n \to \infty } 4 + \frac{100}{n} + \frac{400}{n^{2}} &\leq \lim_{ n \to \infty } c \\
4  \leq c
\end{align}
$$

Given that the required constant $c$ is viable for the definition, $r(n) \in O(g(n))$

## Assumptions

The definition of the [[Asymptotic Upper Bound]] requires that every [[Function]] $f(n)$ and $g(n)$ is asymptotically non-negative, $f(n), g(n)$ must be non-negative whenever $n$ is sufficiently large [^1]

## Properties

### Transitivity Property

The [[Function|Argument]] of an [[Asymptotic Upper Bound]] that is an [[Function|Argument]] of another [[Asymptotic Upper Bound]] can be simplified to just the an [[Asymptotic Upper Bound]] with the innermost [[Function|Argument]] as shown [^2]

$$
f(n) = O(g(n)), g(n) = O(h(n)) \implies f(n) = O(h(n))
$$

### Reflexivity Property

A given [[Function]] $f(n)$ is equal to its [[Asymptotic Upper Bound]] $\Theta(f(n))$ [^2]

$$
f(n) = O(f(n))
$$

### Symmetry Property

Applying the [[#Reflexivity Property]] and [[#Transitivity Property]] results to the assertion that a [[Function]] $f(n)$ is equal to an [[Asymptotic Upper Bound]]$O((n))$ if and only if $g(n) = O(f(n))$ [^2]

$$
f(n) = O(g(n)) \iff g(n) = O(f(n))
$$

## References

[1]: Introduction to Algorithms, pp. 50, 54-55

[2]: Introduction to Algorithms, pp. 61-62
