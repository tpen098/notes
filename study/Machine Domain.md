---
aliases: [Machine Domains]
tags: [computer-organization, computational-thinking]
date created: Sunday, August 23rd 2026, 12:27:08 pm
date modified: Sunday, August 23rd 2026, 12:29:49 pm
---

# Machine Domain

The [[Machine Domain]] is the domain of the problem-solving process that describes a storage medium consisting of serially arranged bits that are organized into [[Address Space|Address Spaces]], and [[Central Processing Unit|Processors]] that allow basic operations [^1]

```mermaid
flowchart TD
	subgraph SG1["Storage Medium"]
		x1["Bits"]
		x1["Bytes"]
		x1["Words"]
	end
	subgraph SG2["Processing Units"]
		y1["Addition"]
		y2["Subtraction"]
		y3["Multiplication"]
		y4["Division"]
		y5["Comparison"]
		y6["..."]
	end
	
	SG1 <--> SG2
```

## Reference

[1]: Data Structures, p. 2
