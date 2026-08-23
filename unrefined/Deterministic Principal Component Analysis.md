---
aliases:
  - Deterministic PCA
tags:
  - machine-learning
date created: Tuesday, November 29th 2022, 6:59:24 pm
date modified: Friday, August 21st 2026, 3:46:33 pm
---

# Deterministic Principal Component Analysis

## Motivation

The [[Principal Component Analysis]] is an [[Algorithm]] for determining a [[Low-Dimensional Encoding]] and [[Low-Dimensional Decoding]] of a given a [[Dataset]] mainly focusing on the [[Model Input]] $\mathcal{X} = \{ x_{1}, \dots, x_{N} \}, x_{n} \in \mathbb{R}^{D}$, with zero [[Mean]] $\mu = 0$ and a [[Covariance|Covariance Matrix]] as shown

$$
S
= \frac{1}{N} \sum_{n=1}^N x_{n} x^{\top},
= \frac{1}{N} X X^{\top}
, X \in \mathbb{R}^{D \times N}
$$

## Centering

Subtract the [[Mean]] of the entire [[Model Input]] [[Dataset]] $\mathcal{X}$ to every [[Model Input]] $x_{i}$ to center the data on the origin

$$
x' = x - \mu
$$

## Standardization

Divide the [[Model Input|Model Inputs]] by the [[Standard Deviation]] $\sigma_{d}$ of the [[Model Input]] [[Dataset]] $\mathcal{X}$ for each dimension $d$ to make the data unitless and normalize the [[Variance]] to $1$ along each axis used.

$$
x'' = \frac{x'}{\sigma}
$$

## Low-Dimensional Encoder and Decoder

The [[Orthonormal]] [[Projection|Projection Matrix]] $B$ required to form the [[Low-Dimensional Decoding|Low-Dimensional Decoder]] $B$ and [[Low-Dimensional Encoding|Low-Dimensional Encoder]] $B^{\top}$ can be derived from the [[Eigendecomposition]] of the [[Model Input]] [[Covariance|Covariance Matrix]] $S$ as follows

$$
S = BDB^{\top}
$$

## Low-Dimensional Projection

Projecting the [[Model Input]] $x$ to a lower-dimension means applying [[Low-Dimensional Encoding]] and [[Low-Dimensional Decoding]] in succession.

$$
\tilde{x}_{norm} = B_{m}B_{m}^{\top}x
$$

## Back Projection

The centering and standardization must be removed to properly present the approximated [[Model Input]]. These processes can be reversed by multiplying the current approximated [[Model Input]] $x_{p}$ with the [[Standard Deviation]] $\sigma$ per dimension and adding back the [[Mean]] $\mu$

$$
\tilde{x}_{n} = \tilde{x}_{norm}\sigma + \mu
$$

## References

1. Mathematics for Machine Learning, Ch. 10, pp. 336-337
