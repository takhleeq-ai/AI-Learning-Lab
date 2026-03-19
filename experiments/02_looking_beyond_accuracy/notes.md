# Week 2 — Looking Beyond Accuracy

## Objective

This experiment explores why accuracy can be misleading when working with imbalanced classification problems.

In many real-world systems, the most important events are not the most common ones. That means a model can appear to perform well overall while still failing to identify the cases that matter most.

## What I tested

I created a simple imbalanced classification dataset and trained a baseline classifier on it.

I then compared:

- Accuracy
- Confusion matrix
- Precision
- Recall
- F1 score

## Why this matters

Accuracy is easy to understand, but it compresses all model behaviour into a single number.

When one class dominates the dataset, that number can hide weak performance on the minority class.

This becomes important in systems where rare events carry higher significance than routine ones.

## Key takeaway

Accuracy is a useful starting point, but it is not enough on its own.

To evaluate a classifier properly, I need to understand:

- what kinds of mistakes the model is making
- whether it is missing important positive cases
- whether false alarms are acceptable in the system context

## Files

- `experiment.ipynb` — notebook for the Week 2 experiment
- `notes.md` — summary of what was tested and learned