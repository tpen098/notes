---
aliases: [Interpretation, Interpretations, Pure Interpretations, Interpreter, Interpreters]
tags: [language]
date created: Wednesday, September 30th 2026, 9:16:41 pm
date modified: Wednesday, September 30th 2026, 9:19:00 pm
---

# Pure Interpretation

## Definition

[[Pure Interpretation]] interprets a [[Language|Programming Language]] using another [[Program]] called [[Pure Interpretation|Interpreter]], with no [[Compilation]]. [^1]

```mermaid

flowchart TD

	A(["Source Program"])
	B(("Interpreter"))
	C[["Input Data"]]
	
	A --> B --> Results
	C --> B

```

## Reference

[1]: Concepts of Programming Languages, Ch. 1, p. 50
