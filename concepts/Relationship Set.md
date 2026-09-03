---
aliases: [Relationship Sets]
tags: [database]
date created: Monday, August 31st 2026, 9:48:32 pm
date modified: Thursday, September 3rd 2026, 8:45:56 pm
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

## Primary Key

- The [[Primary Key]] of the [[Relationship Set]] is the [[Set Union]] of the [[Primary Key|Primary Keys]] of the [[Entity|Entities]] involved. This is applies for [[Many-to-many Mapping Cardinality|Many-to-many]] [[Relationship|Relationships]]. [^2]
- [[One-to-many Mapping Cardinality|One-to-many]] and [[Many-to-one Mapping Cardinality|Many-to-one]] [[Relationship|Relationships]] use the [[Primary Key]] of the "Many" side. [^2]
- [[One-to-one Mapping Cardinality|One-to-one]] [[Relationship|Relationships]] can use any of the [[Primary Key|Primary Keys]] of the involved [[Entity|Entities]] as [[Primary Key]]. [^2]

## References

[^1]: Database System Concepts, pp. 246-247
[1]: Database System Concepts, pp. 257-259
