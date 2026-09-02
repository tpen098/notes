---
aliases:
  - Relationship Sets
tags:
  - database
date created: Monday, August 31st 2026, 9:48:32 pm
date modified: Monday, August 31st 2026, 10:25:24 pm
---

# Relationship

## Definition

A [[Relationship Set]] is a [[Set]] of [[Relationship|Relationships]] of the same type [^1]

## Representation

Formally, the [[Relationship Set]] $R$ is a relation on $n \ge 2$ [[Entity Set|Entity Sets]] $E_{1}, E_{2}, \dots$ such that it is a subset of the following [[Tuple]] [^1]

$$
	\{ 
	(e_{1}, e_{2}, \dots, e_{n}) 
	| e_{1} \in E_{1}, e_{2} \in E_{2}, \dots, e_{n} \in E_{n}
	\}
$$

In this case, $(e_{1}, e_{2}, \dots, e_{n})$ is a [[Relationship Instance]] [^1]

## References

[^1]: Database System Concepts, pp. 246-247
