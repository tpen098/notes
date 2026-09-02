---
aliases: [Search]
tags: [computational-thinking]
date created: Thursday, March 14th 2024, 11:36:52 am
date modified: Sunday, August 23rd 2026, 12:07:17 pm
---

# Search Operation

## Definition

A [[Search Operation]] $SEARCH(S, k)$ is a [[Query Operation]] on a given [[Data Structure]] $S$ with [[Function|Argument]] [[Record|Key]] $k$ that returns a [[concepts/Pointer]] to a [[Record]] of the [[Data Structure]] $x$ such that $x.key = k$. If the [[Record]] is not found in the [[Data Structure]], it returns an [[concepts/Pointer|Empty Pointer]] $NIL$ [^1]

> [!NOTE]
> A variation of the [[Search Operation]] for a [[Data Structure]] $S$ that contains general [[Set Membership|Elements]] $x$ would search for the [[Set Membership|Element]] itself by value $x.value = k$ or the [[Set Membership|Element]] itself $x = k$

## References

[1]: Introduction to Algorithms, p. 250
