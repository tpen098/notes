---
aliases: [Time Switching, Concurrency]
tags: [computer-organization]
date created: Saturday, August 15th 2026, 10:18:56 pm
date modified: Friday, August 21st 2026, 3:38:39 pm
---

# Time Sharing

## Definition

[[Time Sharing]] is a [[Central Processing Unit|CPU]] [[Virtualization]] technique wherein the [[Operating System]] cycle between [[Process|Processes]] very quickly to provide the illusion of parallel execution. Each [[Process]] is given the illusion that the entire [[Central Processing Unit|CPU]] is reserved for them. [^1]

| Process 1 | x   |     |     |     | x   |     |     |     |
| --------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Process 2 |     | x   |     |     |     | x   |     |     |
| Process 3 |     |     | x   |     |     |     | x   |     |
| Process 4 |     |     |     | x   |     |     |     | x   |

## Reference

[^1]: Operating Systems - Three Easy Pieces, p. 25
