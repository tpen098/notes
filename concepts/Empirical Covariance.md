---
aliases: [Empirical Covariances, Population Covariance, Population Covariances, Sample Covariance, Sample Covariances]
tags: [linear-algebra]
date created: Sunday, November 6th 2022, 5:39:47 pm
date modified: Thursday, August 20th 2026, 6:26:41 pm
---

# Empirical Covariance

## ## Definition

The [[Empirical Covariance]] is a [[Symmetric, Positive Semidefinite]] [[Matrix]] representing the [[Covariance]] of the observations in the finite [[Dataset]] $n \in N$ for each [[Variable]] $x_n(n) = [x_{1}(n), \dots, x_{D}(n)]$, defined with the [[Empirical Mean]] as shown in the following

$$
\Sigma :=
\frac{1}{N}
\sum_{n=1}^N (x_{n}-\bar{x})(x_{n}-\bar{x})^{\top}
$$

## Reference

1. Mathematics for Machine Learning, pp. 192-193
