---
aliases: [Storage Managers, Storage Manager Module, Storage Manager Modules]
tags: [database]
date created: Friday, August 21st 2026, 8:55:51 pm
date modified: Friday, August 21st 2026, 9:58:17 pm
---

# Storage Manager

## Definition

The [[Storage Manager]] is the component of the [[Database Engine]] that provides the interface between the low-level data stored in the [[Database]] and the application programs, and the [[Query|Queries]] submitted to the [[Database-Management System]]. It is responsible for the interaction between the file manager by translating [[Data-Definition Language]] statements into low-level file system commands. [^1]

## Components

### Authorization and Integrity Manager

This tests for the satisfaction of integrity constraints and checks the authority of users to access data. [^1]

### File Manager

This manages the allocation of space on disk storage and the data structures used to represent information stored on disk. [^1]

### Buffer Manager

This is responsible for fetching data from disk storage into main memory, and deciding what data to cache in main memory. It enables the database to handle data sizes that are much larger than the size of main memory. [^1]

### Transaction Manager

![[Transaction Management#Definition]]

## Data Structures

### Data Files

Stores the [[Database]] itself.

### Data Dictionary

This stores metadata about the [[Schema|Database Schema]].

### Indices

The [[concepts/Pointer|Indices]] provides fast access to data items.

## Reference

[1]: Database System Concepts, p. 19
