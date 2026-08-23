---
aliases: [Processes, Machine State, Machine States]
tags: [computer-organization]
date created: Saturday, August 15th 2026, 10:13:19 pm
date modified: Sunday, August 23rd 2026, 12:06:51 pm
---

# Process

## Definition

A [[Process]] is a running [[Program]] in an [[Operating System]]. Part of its definition is the parts of the machine that are important for its execution or the [[Process|Machine State]]. It is comprised of the [[Address Space]], registers such as the [[Program Counter]], [[Stack Pointer]], [[Frame Pointer]], and list of files the [[Process]] currently has open. [^1]

## Interface

A [[Process]] must support the following in its [[Application Programming Interface|API]] [^1]

1. **Create:** An [[Operating System]] must enable new [[Process|Processes]] to be created
2. **Destroy:** An [[Operating System]] must enable existing [[Process|Processes]] to be destroyed, either voluntarily or inadvertently.
3. **Wait:** An [[Operating System]] must enable existing [[Process|Processes]] to stop running and wait for a trigger to occur before proceeding
4. **Status:** An [[Operating System]] must provide an interface to get information on a [[Process]]. This can be the state or lifetime metrics of a [[Process]].

## References

[^1]: Operating Systems, - Three Easy Pieces, pp. 36-37.
