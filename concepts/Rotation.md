---
aliases: [Rotated, Rotation Matrix, Rotations, Rotation Matrices]
tags: [linear-algebra]
date created: Thursday, September 22nd 2022, 7:33:54 pm
date modified: Friday, August 21st 2026, 2:44:27 pm
---

# Rotation

## Definition

A [[Rotation]] is a [[Linear Mapping]] that rotates a plane by an [[Angle]] $\theta$ about the origin.

## Convention

- For a positive angle $\theta$, the [[Rotation]] is counter-clockwise
- For a negative angle $\theta$, the [[Rotation]] is clockwise
- For more than two dimensions, counter-clockwise or planar rotation about an axis refers to rotation about an axis when the axis is looked as "head on, from the end towards the origin"

## Low Dimensional Examples

- [[Rotation in 2D]]
- [[Rotation in 3D]]

## Preservation of Distances

[[Distance]] is unchanged after the transformation

$$
\lVert x - y \rVert
=
\lVert R_{\theta}(x) - R_{\theta}(y) \rVert
$$

## Preservation of Angles

[[Angle]] between two vectors is unchanged after the transformation

## Non-commutativity for Higher Dimensions

[[Rotation]] in three dimensions or more are generally not [[Commutative]]. The order of application matters

## References

1. Mathematics for Machine Learning, Ch. 3, pp. 91, 93-94
