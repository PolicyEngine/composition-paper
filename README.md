# composition-paper

Paper and experiment workspace for the composition study: what happens when
survey imputation and weight calibration are *combined*, measured where the
operator papers structurally cannot look. Third leg of the populace
publication portfolio, after the operator dossiers
([imputation-paper](https://github.com/PolicyEngine/imputation-paper),
[calibration-paper](https://github.com/PolicyEngine/calibration-paper),
[sparsity-paper](https://github.com/PolicyEngine/sparsity-paper)) and on the
[popdgp](https://github.com/PolicyEngine/popdgp) referee.

## The four questions (each unanswerable by a single-operator eval)

1. **Realized landmines**: the fragility diagnostic bounds worst-case
   reweighting; here we run actual calibrators on each imputation method's
   file and measure realized tail distortion — the interaction that produced
   the eCPS incident.
2. **Repairability, quantified**: a weight-blind imputation fails in the
   measure with intact support (coverage invariance), so calibration could
   partially repair it. How much of a 2× q99 inflation does
   calibration-to-targets actually claw back, at what weight-concentration
   cost?
3. **The target-vs-survey tug-of-war**: administrative targets and donor
   surveys disagree; calibrating toward targets moves the file away from
   survey-view fidelity. The trade-off curve, reported as a Pareto frontier
   (target attainment vs population-view scores), never scalarized.
4. **Effective-support collapse**: nominal coverage is reweighting-invariant,
   but weight concentration can collapse *effective* support. Weighted
   coverage variants (coverage of the top-99%-of-mass records) exist only at
   the composition.

## Design

Factorial: frontier imputation methods (from imputation-paper) × calibrators
(from calibration-paper) on holdout-masked builds (populace#302), scored on
held-out target families AND survey holdouts via popdgp, floors everywhere.
Bounded grid — the operator papers exist so this one never re-litigates
baselines.

Blocked on: populace#302 (holdout-masked builds), calibration-paper's method
adapters. Venue: Journal of Official Statistics or IJM (diamond OA).
