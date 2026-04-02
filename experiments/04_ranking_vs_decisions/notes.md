# Week 4 — Ranking vs Decisions

## Context

Last week explored how changing the decision threshold affects model behaviour.

This week, I removed the threshold entirely and focused on the model's raw outputs.

## Key Insight

The model does not make decisions.

It produces scores.

Each prediction is a probability — representing how likely an observation is to belong to the positive class.

A binary decision only appears when a threshold is applied on top of these scores.

## Why This Matters

This reframes how models should be evaluated.

The key question is not:

"Is the prediction correct?"

It is:

"How well does the model rank what matters?"

## Experiment Summary

- trained a logistic regression model on an imbalanced dataset
- generated predicted probabilities (`predict_proba`)
- compared binary predictions vs probability scores
- plotted ROC curve
- plotted Precision–Recall curve

## Observations

- binary predictions hide useful information about confidence
- probability scores provide a ranking of observations
- ROC curve shows model behaviour across all thresholds
- Precision–Recall curve is more informative for imbalanced datasets
- models with similar accuracy can behave differently when viewed through ranking

## Real-World Framing

In systems like fraud detection, credit risk, and affordability:

- cases are prioritised based on risk scores
- different score bands trigger different actions
- decisions are layered on top of model outputs

The model supports decision-making — it does not directly decide.

## Key Shift

From:

"Is the prediction correct?"

To:

"How well does the model rank what matters?"

## Limitations

- evaluation is still based on a single model
- no comparison across different models yet
- ROC may appear strong even when performance on positives is weak

## Next Steps

- compare ROC-AUC vs PR-AUC explicitly
- evaluate multiple models for ranking quality
- explore how class imbalance affects interpretation
- connect ranking behaviour to business decision thresholds