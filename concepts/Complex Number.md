---
aliases: [Complex, Complex Numbers, Imaginary, Imaginary Number, Imaginary Numbers, Imaginary Part, Imaginary Parts, Imaginary Unit, Imaginary Units, Real Part, Real Parts, Set of Complex Numbers]
tags: [mathematics]
date created: Friday, March 15th 2024, 10:22:41 am
date modified: Tuesday, August 18th 2026, 9:31:23 pm
---

# Complex Number

## Definition

A [[Complex Number]] is an [[concepts/Expression]] containing the [[Complex Number|Real Part]] or [[Real Number]] $a$ plus the [[Complex Number|Imaginary Part]] or another [[Real Number]] $b$ multiplied by the [[Complex Number|Imaginary Unit]] $i = \sqrt{ -1 }$ as shown [^1]

$$
c = a + b i
$$

## Operations

### Addition and Subtraction

When adding or subtracting [[Complex Number|Complex Numbers]], the resulting [[Complex Number]] has the sum or difference of the [[Complex Number|Real Parts]] as its [[Complex Number|Real Part]] and has the sum or difference of the [[Complex Number|Imaginary Parts]] as its [[Complex Number|Imaginary Part]] [^1]

$$
\sum_{k=1}^{n} (a_{k} \pm b_{k} i) = \sum_{k=1}^{n} a_{k} \pm i \sum_{k=1}^{n} b_{k}
$$

### Multiplication

Multiplying two [[Complex Number|Complex Numbers]] is similar to multiplying [[Binomial|Binomials]] [^1]

$$
(a + bi) \cdot (c + d i) = ac + adi + bci + bd i^{2} 
$$

Given that $i = \sqrt{ -1 } \implies i^{2} = -1$, the [[concepts/Expression]] can be further simplified to the following [^1]

$$
ac + adi + bci - bd \atop
(ac - bd) + (ad + bc)i
$$

### Division

To simplify the quotient $\dfrac{{a + bi}}{c + di}$, the [[concepts/Expression]] can be multiplied with a fraction wherein the numerator and the denominator is the [[Complex Conjugate]] of the quotient's denominator so that it is technically multiplied by $1$ [^1]

$$
\dfrac{{a + bi}}{c + di} \cdot 1 = \dfrac{{a + bi}}{c + di} \cdot \dfrac{{c - di}}{c - di}
$$

This results in an [[concepts/Expression]] wherein the numerator is a [[Complex Number]] and the denominator is purely [[Real Number|Real]] [^1]

$$
\frac{(ac + bd) + (bc - ad)i}{c^2 + d^2}
$$

## References

[1]: Precalculus - Calculus for Mathematics, pp. 59-61
