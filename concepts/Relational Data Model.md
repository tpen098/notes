---
aliases: [Relational Data Models, Relational Model, Relational Models, Relational Data, Relation, Relations]
tags: [database]
date created: Friday, August 21st 2026, 5:18:36 pm
date modified: Friday, August 21st 2026, 5:56:14 pm
---

# Relational Data Model

## Definition

A [[Relational Data Model]] is a [[Record-Based Model]] that uses a collection of tables called [[Relational Data Model|Relations]] to represent both data and relationships among these data. Each [[Relational Data Model|Relation]] consists of multiple columns, each with a unique name. [^1]

## Example

 The following is an example of a [[Relational Data Model|Relation]] for Instructors.

| ID   | name     | department_name | salary |
| ---- | -------- | --------------- | ------ |
| 2222 | Einstein | Physics         | 95000  |
| 1211 | Wu       | Finance         | 90000  |
| 3231 | El Said  | History         | 60000  |

Here is another example of a [[Relational Data Model|Relation]] for Departments

| department_name  | building | budget  |
| ---------------- | -------- | ------- |
| Computer Science | Taylor   | 100000  |
| Biology          | Watson   | 90000   |
| Finance          | Packard  | 1200000 |

Notice that the two [[Relational Data Model|Relations]] have a common column `department_name` that relates the two [[Relational Data Model|Relations]] or table.

## References

[^1]: Database System Concepts, p. 8
