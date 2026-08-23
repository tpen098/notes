---
aliases: [Asymptotically Tight Bounds, Average-Case, Average-Case Complexity]
tags: [optimization]
date created: Thursday, March 14th 2024, 2:21:12 pm
date modified: Tuesday, August 18th 2026, 9:06:23 pm
---

# Asymptotically Tight Bound

## Definition

The [[Asymptotically Tight Bound]] $\Theta$-notation is the [[Function]] $\Theta(\cdot)$ that takes a [[Function]] $g(n)$ to produce the [[Set]] of [[Function|Functions]] $\Theta(g(n))$ containing [[Function|Functions]] $f(n)$ such that $c_{1} g(n) \leq f(n) \leq c_{2} g(n)$ for sufficiently large $n$ [^1]

$$
\forall n \geq n_{0}, \Theta(g(n)) = \{ 0 \leq c_{1} g(n) \leq f(n) \leq c_{2} g(n)\}
$$

## Intuition

The [[Asymptotically Tight Bound]] combines the intuition of the [[Asymptotic Lower Bound]] and the [[Asymptotic Upper Bound]] by stating that the running time $r(n)$ is close to the [[Function]] $g(n)$ to within constants $c_{1}, c_{2}$ [^1]

In fact, for any two [[Function|Functions]] $f(n), g(n)$, $f(n) = \Theta(g(n))$ if and only if $f(n) = O(g(n)), \Omega(g(n))$

$$
f(n) = \Theta(g(n)) \iff f(n) = O(g(n)), f(n) = \Omega(g(n))
$$

## Properties

### Transitivity Property

The [[Function|Argument]] of an [[Asymptotically Tight Bound]] that is an [[Function|Argument]] of another [[Asymptotic Upper Bound]] can be simplified to just the an [[Asymptotically Tight Bound]] with the innermost [[Function|Argument]] as shown [^2]

$$
f(n) = \Theta(g(n)), g(n) = \Theta(h(n)) \implies f(n) = \Theta(h(n))
$$

### Reflexivity Property

A given [[Function]] $f(n)$ is equal to its [[Asymptotically Tight Bound]] $\Theta(f(n))$ [^2]

$$
f(n) = \Theta(f(n))
$$

### Symmetry Property

Applying the [[#Reflexivity Property]] and [[#Transitivity Property]] results to the assertion that a [[Function]] $f(n)$ is equal to an [[Asymptotically Tight Bound]] $\Theta((n))$ if and only if $g(n) = \Theta(f(n))$ [^2]

$$
f(n) = \Theta(g(n)) \iff g(n) = \Theta(f(n))
$$

## References

[1]: Introduction to Algorithms, pp. 51, 55-56
[2]: Introduction to Algorithms, pp. 61-62
