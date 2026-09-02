---
aliases: [Relationship Sets]
tags: [database]
date created: Monday, August 31st 2026, 9:48:32 pm
date modified: Wednesday, September 2nd 2026, 1:45:33 pm
---

# Relationship

## Definition

A [[Relationship Set]] is a [[Set]] of [[Relationship|Relationships]] for the same type [^1]

## Representation

Formally, the [[Relationship Set]] $R$ is a relation on $n \ge 2$ [[Entity Set|Entity Sets]] $E_{1}, E_{2}, \dots$ such that it is a subset of the following [[Tuple]] [^1]

$$
	\{ 
	(e_{1}, e_{2}, \dots, e_{n}) 
	| e_{1} \in E_{1}, e_{2} \in E_{2}, \dots, e_{n} \in E_{n}
	\}
$$

In this case, $(e_{1}, e_{2}, \dots, e_{n})$ is a [[Relationship Instance]] [^1]

> [!INFO] Example
> Consider an [[Entity Set]] for students $E_{s}$ and instructors $E_{I}$. With the [[Relationship Set]] Advisor $A$, a tuple of a student and instructor $(e_{s}, e_{i})$ is within the [[Relationship Set]] $(e_{s}, e_{i}) \in A$

## References

[^1]: Database System Concepts, pp. 246-247
