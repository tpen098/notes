---
aliases:
  - Common Logarithm
  - Common Logarithm Function
  - Common Logarithm Functions
  - Common Logarithms
  - Logarithm
  - Logarithms
  - Natural Logarithm
  - Natural Logarithm Function
  - Natural Logarithm Functions
  - Natural Logarithms
tags:
  - mathematics
date created: Friday, March 15th 2024, 12:59:21 pm
date modified: Friday, March 15th 2024, 1:20:03 pm
---

## Definition

The [[Logarithm Function]] $\log_{a} x$ is the [[Inverse]] [[Function]] of the [[Exponential Function]] that, given a [[Variable]] [[Function|Argument]] $x$, returns the [[Exponent]] $y$ needed for a [[Exponent|Base]] $a$ to equal $x$ [^1]

$$
f(x) = \log_{a} x = y \iff f'(x) = x = a^{y}
$$

## Common Definition

The usual definition of the [[Logarithm Function]] is the [[Logarithm Function|Common Logarithm Function]], which is a [[Logarithm Function]] with [[Exponent|Base]] $10$ [^2]

$$
f(x) = \log_{10}x = \log x
$$

## Natural Definition

Another common variant of the [[Logarithm Function]] is the [[Logarithm Function|Natural Logarithm Function]], which is a [[Logarithm Function]] with [[Exponent|Base]] being [[Euler's Number|Euler Number]] $e$ [^3]

$$
f(x) = \log_{e} x = \ln x
$$

## Law of Logarithms

### Product Arguments and Logarithm Addition

The [[Logarithm Function|Logarithm]] of a product of two [[Real Number|Real Numbers]] $ab$ is the sum of [[Logarithm Function|Logarithms]] of the given [[Real Number|Real Numbers]] [^4]

$$
\log_{a}(xy) = \log_{a} x + \log_{a} y
$$

### Quotient Arguments and Logarithm Difference

The [[Logarithm Function|Logarithm]] of a quotient of two [[Real Number|Real Numbers]] $\dfrac{a}{b}$ is the difference of [[Logarithm Function|Logarithms]] of the given [[Real Number|Real Numbers]] [^4]

$$
\log_{a} \dfrac{x}{y} = \log_{a} x - \log_{b} y
$$

### Argument Powers and Scaling

The [[Exponent]] of an [[Function|Argument]] $c$ can be removed from the [[Function|Argument]] to be a scaling factor of the [[Logarithm Function|Logarithm]] [^4]

$$
\log_{a}(x^{c}) = c \log_{a} x
$$

### Change of Base Formula

Given a [[Logarithm Function|Logarithm]] with [[Exponent|Base]] $a$, the [[Exponent|Base]] can be changed to $b$ by dividing it with a [[Logarithm Function|Logarithm]] with [[Exponent|Base]] $a$ and [[Function|Argument]] $b$ [^4]

$$
\log_{a} x 
\to \dfrac{\log_{a} x}{\log_{a} b} 
= \log_{b} x
$$

An extension of this rule is that if $a =1$ and $x = a$, then the formula can be reinterpreted such that inverting the [[Exponent|Base]] and the [[Function|Argument]] can be done by getting the [[Reciprocal]] first [^4]

$$
\log_{b} a = \dfrac{1}{\log_{a} b}
$$

## References

[1]: Precalculus - Mathematics for Calculus, p. 334

[2]: Precalculus - Mathematics for Calculus, p. 348

[3]: Precalculus - Mathematics for Calculus, p. , 349

[4]: Precalculus - Mathematics for Calculus, pp. 354, 357
