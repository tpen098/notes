---
aliases: []
tags: [computational-thinking]
date created: Thursday, August 13th 2026, 7:55:22 pm
date modified: Sunday, August 23rd 2026, 11:51:52 am
---

# Definition

Given a problem $Q$, and an input $x$, determine whether $Q$ will halt on $x$

## Unsolvability

Using [[Proof by Contradiction]]:

1. Assume a program $A$ that takes a program $P_{a}$ and input $x_{a}$.
	- Returns True if the code eventually halts
	- Returns False if the code never halts
2. With program $B$ that takes a program $P_{b}$. This will be designed to naturally contradict $A$ later on. It's definition is defined as:
	- Does not halt if $A(P_{b}, P_{b})$ returns True
	- Halts if $A(P_{b}, P_{b})$ returns False
3. Running $B(B)$ leads to a contradiction:
	- If $A$ predicts $B$ will halt such that $A(P_{b}, P_{b}) = A(B, B)$ is True, then $B$ actually does halts by its definition
	- If $A$ predicts $B$ will not halt such that $A(P_{b}, P_{b}) = A(B, B)$ is False, then $B$ actually halts by its definition
