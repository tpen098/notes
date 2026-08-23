---
aliases: [Arrays]
tags: [computational-thinking]
date created: Thursday, March 14th 2024, 12:58:08 pm
date modified: Sunday, August 23rd 2026, 12:05:53 pm
---

# Array

## Definition

The [[Array]] is a fixed-size, [[Contiguous Data Structure]] of [[Set Membership|Elements]] with the same type, defined as a [[Finite Sequence]] of [[Record|Records]] wherein the [[Record|Keys]] are sequential [[Pointer|Indices]], represented using the [[Whole Number|Set of Whole Numbers]] $\mathbb{W}$ [1]

```mermaid

stateDiagram-v2
direction LR

state Array {	

	0 --> block00
	1 --> block01
	2 --> block02
}

state "Element 0" as block00 {
	state "Value 0" as value00
}

state "Element 1" as block01 {
	state "Value 01" as value01
}

state "Element 2" as block02 {
	state "Value 02" as value02
}
```

If the first [[Set Membership|Element]] of an [[Array]] starts at memory address $a$, and each [[Set Membership|Element]] takes $b$ bytes, then the $i-th$ [[Set Membership|Element]] occupies bytes $a + bi$ to $a + bi + b - 1$ [^2]

## Record Access

Given the corresponding [[Pointer|Index]] of a [[Record]], direct access can be done in [[Asymptotic Upper Bound|Worst-Case]] constant running time $O(1)$ [^1]

## References

[1]: The Algorithm Design Manual, p. 70
[2]: Introduction to Algorithms, p. 252
