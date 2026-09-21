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
held-out target families AND survey holdouts via popdgp, with declared support
and target-family floors.
Bounded grid — the operator papers exist so this one never re-litigates
baselines.

For US and UK poverty, survey estimates serve only as comparison diagnostics.
Poverty rates and counts do not enter calibration targets, held-out target
scores, candidate rankings, parameter selection or release thresholds. Do not
choose weights, imputations, support or a build to reduce a poverty gap,
including through informal inspection of the trade-off curves. The support
and target-family floors above do not apply to poverty comparisons.

Report the poverty definition, population, income period and weight basis for
each comparison. Correct measurement or implementation errors using
independently justified evidence and retain the remaining differences in the
results. Separately justified income and benefit targets remain distinct from
poverty estimates.

Blocked on: populace#302 (holdout-masked builds), calibration-paper's method
adapters. Venue: Journal of Official Statistics or IJM (diamond OA).

## License

Code in this repository is released under the [MIT License](LICENSE). Original text and figures are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) with attribution to PolicyEngine. Third-party data and materials keep their own terms.
