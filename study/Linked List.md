---
aliases: [Doubly Linked List, Doubly Linked Lists, Head, Heads, Linked Lists, List, Lists, Next Pointer, Next Pointers, Prev Pointer, Prev Pointers, Previous Pointer, Previous Pointers, Singly Linked List, Singly Linked Lists, Tail, Tails]
tags: [computational-thinking]
date created: Friday, March 15th 2024, 3:55:41 pm
date modified: Sunday, August 23rd 2026, 1:19:30 pm
---

# Linked List

## Definition

A [[Linked List]] is a [[Linked Data Structure]] that has a starting [[Node]], called a [[Linked List|Head]], and a final [[Node]] node called [[Linked List|Tail]][^1]

### Singly Linked Definition

A [[Linked List|Singly Linked List]] has nodes that can only have a single [[concepts/Pointer]], often called the [[Linked List|Next Pointer]], to another, distinct node that has not been pointed to in the [[Linked List]] so far. The [[Linked List|Tail]] has a [[concepts/Pointer|Null Pointer]] as its [[Linked List|Next Pointer]] [^1]

```mermaid
stateDiagram-v2
direction LR

state Head {
	data0
	next0
}

state Node1 {
	data1
	next1
}

state Node2 {
	data2
	next2
}

state Node3 {
	data3
	next3
}

state Tail {
	data4
	next4
}

[*] --> Head
next0 --> Node1
next1 --> Node2
next2 --> Node3
next3 --> Tail
next4 --> [*]
```

### Doubly Linked Definition

A [[Linked List|Doubly Linked List]] has nodes that can have two [[concepts/Pointer|Pointers]], a [[Linked List|Next Pointer]], which is still restricted to pointer to another distinct node, and a [[Linked List|Previous Pointer]], which points to the node that has the current node in its [[Linked List|Next Pointer]] [^1] In this case, the [[Linked List|Head]]'s [[Linked List|Previous Pointer]] is a [[concepts/Pointer|Null Pointer]] by definition.

```mermaid
stateDiagram-v2
direction LR

[*] --> Head

state Head {
	prev0
	next0
	data0
}

state Node1 {
	prev1
	next1
	data1
}

state Node2 {
	prev2
	next2
	data2
}

state Tail {
	prev3
	next3
	data3
}

next0 --> Node1
next1 --> Node2
next2 --> Tail

prev1 --> Head
prev2 --> Node1
prev3 --> Node2

next3 --> [*]
```

## References

[1]: The Algorithm Design Manual, p. 72
