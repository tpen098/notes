---
aliases: []
tags:
  - mathematics
date created: Wednesday, March 13th 2024, 9:01:29 am
date modified: Sunday, August 16th 2026, 4:32:18 pm
---

# Principle of Inclusion and Exclusion

## Statement

The [[Principle of Inclusion and Exclusion]] states that the [[Set Cardinality]] of a [[Set Union]] of a [[Set Collection]] $\lvert A_{1} \cup A_{2} \cup \dots \cup A_{n} \rvert$ consists of the sum of the [[Set Cardinality]] of every [[Set Intersection]] of every [[Combination]] from the [[Set Collection]], wherein the term is positive if the [[Set Union]] has an odd number of operands, else it is negative as shown below [^1]

$$
\begin{align}
\left\lvert \bigcup _{i=1}^{n} A_{i} \right\rvert =
&+\lvert A_{1} \rvert + \lvert A_{2} \rvert + \dots + \lvert A_{n} \rvert\\
&- \lvert A_{1} \cap A_{2} \rvert - \lvert A_{2} \cap A_{3} \rvert - \lvert A_{1} \cap A_{3} \rvert - \dots \\
&+ \lvert A_{1} \cap A_{2} \cap A_{3} \rvert + \lvert A_{1} \cap A_{2} \cap A_{4} \rvert + \dots \\
&\dots \\
& + (-1)^{n-1} \lvert A_{1} \cap A_{2} \cap \dots \cap A_{n} \rvert
\end{align}
$$

## Examples

### Application on Two Sets

$$
\lvert A \cup B \rvert 
= \lvert A \rvert + \lvert B \rvert - \lvert A \rvert
$$

### Application on Three Sets

$$
\begin{align}
\lvert A \cup B \cup C \rvert 
&= \lvert A \rvert + \lvert B \rvert + \lvert C \rvert \\
&- \lvert A \cap B \rvert - \lvert A \cap C \rvert - \lvert B \cap C \rvert \\
&+ \lvert A \cap B \cap C\rvert
\end{align}
$$

## References

[1]: Introduction to Algorithms, p. 1158
