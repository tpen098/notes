---
aliases: [Descriptive Attributes]
tags: [database]
date created: Monday, August 31st 2026, 10:28:31 pm
date modified: Monday, August 31st 2026, 10:32:34 pm
---

# Descriptive Attribute

## Definition

A [[Descriptive Attribute]] is an [[Attribute]] of a [[Relationship]]. [^1]

## Representation

Visually, a [[Descriptive Attribute]] can be represented as its own square, but connected to the [[Relationship Instance]] via a dotted line.

![[Descriptive Attribute.png]]

Using a standard [[Entity-Relationship Data Model|Entity-Relationship Model]] diagram, it's represented as another [[Entity]]

```mermaid
erDiagram
    STUDENT ||--o{ TAKES : records
    SECTION ||--o{ TAKES : includes
    
    STUDENT {
        string student_id PK
        string name
        int tot_cred
    }
    
    SECTION {
        string section_id PK
        string course_id
        string semester
        int year
    }
    
    TAKES {
        string student_id FK
        string section_id FK
        string grade
    }

```

## References

[^1]: Database System Concepts, p. 246
[^2]: Database System Concepts, p. 248
