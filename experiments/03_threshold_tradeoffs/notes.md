# Week 3 — Thresholds and the Cost of Being Wrong

## Context

The dataset is imbalanced, with far fewer positive cases than negative ones.

Initial model evaluation showed high accuracy (~94%), but something felt off.

## Key Observation

At the default threshold (0.5):

- the model predicted almost all cases as negative
- accuracy appeared high
- but recall for the positive class was effectively zero

The model was "accurate", but not useful.

## Threshold Experiment

By lowering the decision threshold:

- recall increased (more positive cases detected)
- false positives increased
- precision decreased

The model behaviour changed significantly without changing the model itself.

## Key Insight

The model did not change.

The decision changed.

Threshold selection directly affects:

- false positives
- false negatives
- overall system behaviour

## Why This Matters

In real-world systems:

- missing a positive case (false negative) can be costly (e.g. fraud)
- flagging a negative case (false positive) may be tolerable

This means:

Choosing a threshold is not just a technical decision.

It is a product and risk decision.

## Real-World Framing

In fraud detection:

- lower threshold → catch more fraud, but increase alerts
- higher threshold → fewer alerts, but more fraud slips through

The "correct" threshold depends on cost and risk tolerance.

## Key Question

What kind of wrong can the system afford?

## Limitations Observed

- accuracy alone was misleading
- model evaluation depends heavily on threshold choice
- behaviour changes even when model remains unchanged

## Bridge to Week 4

If threshold defines the decision…

Then what does the model actually produce?

## Next Steps

- analyse raw model outputs (probabilities)
- move from decisions to scores
- explore ranking behaviour using ROC and Precision–Recall curves