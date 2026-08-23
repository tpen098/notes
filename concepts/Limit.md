---
aliases: [Limits]
tags: [mathematics]
date created: Friday, March 15th 2024, 1:20:35 pm
date modified: Friday, August 21st 2026, 10:06:06 am
---

# Limit

## Definition

The [[Limit]] of a [[Function]] $f(x)$ as the [[Function|Argument]] $x$ approaches or is arbitrarily close to $a$ results to the [[Function]] [[Function|Value]] that is sufficiently close but not equal to $L$ [^1]

$$
\lim_{ x \to a } f(x) = L
$$

## Double Definition

The [[Limit]] of a [[Function]] $f(x)$ is $L$ as $x$ approaches $a$ if and only if the same is true for the [[Left-Hand Limit]] and the [[Right-Hand Limit]] [^1]

$$
\lim_{ x \to a } f(x) = L \iff 
\lim_{ x \to a^{-} } f(x) = L
\text{ and }
\lim_{ x \to a^{+} } f(x) = L
$$

## Limit Laws

### Limit of a Sum

The [[Limit]] of a sum of [[Function|Functions]] is the sum of the [[Limit|Limits]] of the [[Function|Functions]] [^2]

$$
\lim_{ x \to a } f(x) + g(x) 
= \lim_{ x \to a } f(x)
+ \lim_{ x \to a } g(x)
$$

### Limit of a Difference

The [[Limit]] of a difference of [[Function|Functions]] is the difference of the [[Limit|Limits]] of the [[Function|Functions]] [^2]

$$
\lim_{ x \to a } f(x) - g(x) 
= \lim_{ x \to a } f(x)
- \lim_{ x \to a } g(x)
$$

### Limit of a Constant Multiple

The [[Limit]] of a [[Function]] multiplied by a constant $c$ is the constant multiplied by the [[Limit]] of the [[Function]] [^2]

$$
\lim_{ x \to a } c f(x) = c \lim_{ x \to a } f(x)
$$

### Limit of a Product

The [[Limit]] of a product of [[Function|Functions]] is the product of the [[Limit|Limits]] of the [[Function|Functions]] [^2]

$$
\lim_{ x \to a } f(x) g(x) 
= \lim_{ x \to a } f(x) \lim_{ x \to a } g(x)
$$

### Limit of a Quotient

The [[Limit]] of a quotient of [[Function|Functions]] is the quotient of the [[Limit|Limits]] of the [[Function|Functions]] [^2]

$$
\lim_{ x \to a } \dfrac{f(x)}{g(x)} 
= \dfrac{\lim_{ x \to a } f(x)}{\lim_{ x \to a } g(x) }
$$

### Limit of a Power

The [[Limit]] of an [[Exponent]] of a [[Function]] is the [[Exponent]] of the [[Limit]] of the [[Function]] [^2]

$$
\lim_{ x \to a } (f(x))^{n} 
= \left( \lim_{ x \to a } f(x) \right)^{n},
n \in \mathbb{Z}^+
$$

### Limit of a Root

The [[Limit]] of a [[Equation|Root]] of a [[Function]] is the [[Equation|Root]] of the [[Limit]] of the [[Function]] [^2]

$$
\lim_{ x \to a } \sqrt[n]{f(x)} 
= \sqrt[n]{ \lim_{ x \to a } f(x) }, 
n \in \mathbb{Z}^+
$$

## References

[1]: Precalculus - Mathematics for Calculus, pp. 898, 903
[2]: Precalculus - Mathematics for Calculus, pp. 906-907
