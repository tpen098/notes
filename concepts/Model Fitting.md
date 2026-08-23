---
aliases: [Overfitting, Underfitting, Fitting, Capacity]
tags: [machine-learning]
date created: Sunday, November 13th 2022, 6:04:28 pm
date modified: Friday, August 21st 2026, 2:11:12 pm
---

# Model Fitting

## Statement

The [[Model Fitting|Capacity]] or ability of a [[Machine Learning Model|Model]] to fit a wide variety of [[Function|Functions]] results to the type of [[Model Fitting|Fitting]] that occurs with the [[Machine Learning Model|Model]].

| Capacity          | Fitting Type    | Error (Train) | Error (Test) |
| ----------------- | --------------- | ------------- | ------------ |
| Low Capacity      | Underfitting    | High Error    | High Error   |
| High Capacity     | Overfitting     | Low Error     | High Error   |
| Moderate Capacity | Optimal Fitting | Low Error     | Low Error             |

![[Model Fitting.png]]

## Underfitting

If the [[Machine Learning Model|Predictor]] has too low [[Model Fitting|Capacity]] to represent a [[Function]] that closely resembles the training [[Dataset]] or the testing [[Dataset]], then both yields poor predictions or high values of the [[Loss Function]] or [[Empirical Risk]]. The [[Machine Learning Model|Model]] has not sufficiently "learned".

> [!tip] Increasing Parameters
> To prevent [[Model Fitting|Underfitting]], the [[Machine Learning Model|Model]] needs an increase on the number of parameters for better representation of possible functions.

## Overfitting

The [[Machine Learning Model|Predictor]] can reach a point wherein it fits too closely with a given training [[Dataset]] such that using another [[Dataset]] on the pre-trained [[Machine Learning Model|Model]] results in poor predictions or high values of the [[Loss Function]] or [[Empirical Risk]]. The [[Machine Learning Model|Model]] has too high [[Model Fitting|Capacity]] and "memorized" the training [[Dataset]].

> [!tip] Preventing Overfitting
> To prevent [[Model Fitting|Overfitting]], [[Regularization]] is often used with the given [[Machine Learning Model|Model]].

## Optimal Fitting

The [[Machine Learning Model|Predictor]] doesn't suffer from either [[Model Fitting|Underfitting]] nor [[Model Fitting|Overfitting]]. The [[Model Fitting|Capacity]] is not too specific to the training [[Dataset]] nor too general for other similar [[Dataset|Datasets]]. Ideally yields good predictions or low values of the [[Loss Function]] or [[Empirical Risk]].

## References

1. Mathematics for Machine Learning, pp. 270-272)
