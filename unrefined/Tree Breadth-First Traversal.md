---
aliases: []
tags: [computational-thinking]
date created: Sunday, August 16th 2026, 1:16:28 pm
date modified: Sunday, August 23rd 2026, 12:04:02 pm
---

# Tree Breadth-First Traversal

## Example

Consider the simple binary tree below

```mermaid
graph TB;
    A((a))-->B((b))
    A-->C((c));
    B-->D((d))
    B-->E((e))
    C-->F((f))
```

The result of the Breadth-First Traversal will be as follows

```c++
output = a, b, c, d, e, f
```

> [!NOTE]+
> No recursive approach due to its reliance on a queue system

## Algorithm

### Initial

Initialize a queue and place the root.

### Iteration

While the queue is not empty:
 1. Pop the queue and display, check, or store the popped node's value
 2. Add the children of the popped node from leftmost to rightmost (if any)

### Worst Case Complexities

**Time :** $O(n)$
**Space :** $O(n)$
