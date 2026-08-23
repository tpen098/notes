---
aliases: []
tags: [computational-thinking]
date created: Thursday, August 13th 2026, 8:29:27 pm
date modified: Sunday, August 23rd 2026, 11:51:03 am
---

# Euclid's Algorithm

## Description

An [[Algorithm]] for finding the [[Greatest Common Divisor]] of two [[Integer|Positive Integers]] $m$ and $n$

## Definition

1. Divide $m$ by $n$ and let $r$ be the remainder
2. If $r$ is zero, return $GCD=n$
3. Set $m \leftarrow n, n \leftarrow r$ and go back to step 1

## Example

Let $m=48, n=18$. The [[Greatest Common Divisor]] is $GCD=6$ given the use of [[Euclid's Algorithm]]

### Iteration 1

* **Step 1:** Divide $48$ by $18$.

  $$48 = (18 \times 2) + 12$$

  The remainder is $r = 12$.
* **Step 2:** $r \neq 0$, so skip to step 3.
* **Step 3:** Set $m \leftarrow 18$, $n \leftarrow 12$.

### Iteration 2

* **Step 1:** Divide $18$ by $12$.

  $$18 = (12 \times 1) + 6$$

  The remainder is $r = 6$.
* **Step 2:** $r \neq 0$, so skip to step 3.
* **Step 3:** Set $m \leftarrow 12$, $n \leftarrow 6$.

### Iteration 3

* **Step 1:** Divide $12$ by $6$.

  $$12 = (6 \times 2) + 0$$

  The remainder is $r = 0$.
* **Step 2:** $r = 0$. Return $\textbf{GCD} = 6$.
