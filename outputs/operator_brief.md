# Operator Brief: Ritivel

Ritivel gets a local, deterministic pressure test around product, promises, and level. The useful part is not the dashboard; it is the repeatable evidence path from fixture to failure to operator action.

## Highest-leverage checks

- product evidence replay -> block release until cited evidence is regenerated (product_coverage, evidence ev_0044).
- traceability operator packet -> accept only if decision claims cite fixture evidence (promises_risk, evidence ev_0011).
- level regression harness -> open a regression issue with trace and benchmark delta (level_precision, evidence ev_0110).
- promises boundary probe -> route to reviewer with evidence packet (traceability_latency, evidence ev_0121).

## What makes this useful

The workflow is intentionally local and deterministic. A reviewer can run the same fixture set, inspect the evidence IDs, open the dashboard, and see exactly why a recommendation passed, went to review, or blocked.
