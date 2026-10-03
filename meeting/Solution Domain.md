---
aliases: [Solution Domains]
tags: [computational-thinking]
date created: Sunday, August 23rd 2026, 12:31:27 pm
date modified: Sunday, August 23rd 2026, 12:36:17 pm
---

# Solution Domain

The [[Solution Domain]] is the domain of the problem-solving process that links the [[Problem Domain]] with the [[Machine Domain]]. It consists of two components: [^1]
- [[Data Structure|Data Structures]] to represent higher level data representations into the level understandable for the [[Machine Domain]]
- [[Algorithm|Algorithms]] built from the basic operations of the [[Machine Domain]] to manipulate the [[Domain|Inputs]] of the [[Problem Domain]] into the expected [[Codomain|Outputs]]

```mermaid
flowchart LR
	subgraph SG1["Data Structures"]
		direction LR;
		Lists
		Trees
		Graphs
	end
	subgraph SG2["Algorithms"]
		direction LR;
		Searching
		Sorting
		Traversal
	end
		
	SG1 <--> SG2
```

## Reference

[1]: Data Structures, p. 2
