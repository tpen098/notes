---
aliases: [Compilation Implementation, Compiler, Compilers, Compiler Implementation, Compiler Implementations]
tags: [language]
date created: Wednesday, September 30th 2026, 9:03:48 pm
date modified: Wednesday, September 30th 2026, 9:25:33 pm
---

# Compilation

## Definition

[[Compilation]] is a method wherein [[Program|Programs]] can be translated into machine language that can be executed directly on the computer. [^1]

## Process

The process is defined as the following:

```mermaid

flowchart TD

	A(["Source Program"])
	B["Lexical Analyzer"]
	C["Syntax Analyzer"]
	D["Intermediate Code Generator and Semantic Analyzer"]
	E["Symbol Table"]
	F["Optimization"]
	G["Code Generator"]
	H["Computer"]
	I[["Results"]]
	J[["Input Data"]]
	
	A --> B -- Lexical Analyzer --> C -- Parse Trees --> D -- Intermediate Code --> G -- Machine Language --> H --> I
	
	B --> E
	E --> D
	D --> F
	F -- Intermediate Code --> G
	J --> H
```

## Reference

[1]: Concepts of Programming Languages, Ch. 1, p. 47
