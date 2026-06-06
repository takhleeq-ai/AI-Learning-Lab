# Week 5 — Thresholds as Product Decisions

## What I explored

This week I explored how changing a classification threshold changes the behaviour of a decision system.

The model stayed the same.

The probability scores stayed the same.

Only the threshold changed.

## Why this matters

A classification model usually produces a score, not a final decision.

The threshold turns that score into an action.

In fintech, that action could be:

- approve
- reject
- block
- allow
- send to manual review

## What changed when the threshold moved

At a lower threshold, the system flagged more cases.

This may catch more risky cases, but it can also increase false positives.

At a higher threshold, the system became more selective.

This may reduce false positives, but it can also increase false negatives.

## Fintech interpretation

In fraud detection, a lower threshold may catch more fraud but block more genuine customers.

In affordability checks, a stricter threshold may reduce risky lending but also send more customers into manual review.

In onboarding, threshold choices affect conversion, friction, and operational workload.

## Key takeaway

A model produces a score.

A threshold turns that score into a product decision.

Threshold design is not just technical.

It is a product, risk, and business decision.