---
aliases:
  - Associative Arrays
  - Key
  - Keys
  - Value
  - Values
tags:
  - data-type
date created: Wednesday, September 30th 2026, 11:11:22 pm
date modified: Wednesday, September 30th 2026, 11:13:34 pm
---

# Associative Array

## Definition

An [[Associative Array]] is an unordered collection of data elements that are [[Pointer|Indexed]] by an equal number of values called keys. [^1]

```mermaid

stateDiagram-v2
direction LR

state AssociativeArray {	

	key0 --> block00
	key1 --> block01
	key2 --> block02
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

## Reference

[1]: Concepts in Programming Languages, Ch. 6
