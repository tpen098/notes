---
aliases: []
tags: [computational-thinking]
date created: Sunday, August 16th 2026, 1:16:27 pm
date modified: Sunday, August 23rd 2026, 12:05:22 pm
---

# Tree Running Operation

The generalization of applying a singular operation to every node. The order of application mustn't matter. The method usually utilizes [Recursion](Recursion.md) for conciseness. However, an iterative approach will also work.

> [!Example]+
> Examples of this include running sum of a tree's node values, running product, global equality check, inclusion check, etc.

## Recursive Algorithm

### Base Case

1. If the current root is null, return the default, null, or zero value (depends on operation)
2. Additional recursion skips (example: predefined values at specific operations)

### Recursive Step

Return the operation of all the children of the current node while applying this recursive function to each

> [!NOTE]+
> The root may be altered or not be involved in the whole operation.

### Worst Case Complexities

**Time :** $O(n)$ assuming constant time operation
**Space :** $O(n)$ from the function stac
