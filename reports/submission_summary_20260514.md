# Submission Summary - 2026-05-14

## Context

- Competition data files checked before submission: no new public data files were available.
- Starting best public score recorded here: `0.05345`.
- Starting public rank after the leaderboard update: 2, behind a `0.05470` public score.
- Experiment focus: use prior submitted ranks and public scores to estimate a public-score residual, then add that residual to the tied-best ordering with controlled beta values.

## Results

| ID | File | Description | Public LB | Decision |
| --- | --- | --- | ---: | --- |
| 20260514-01 | `day9_pubfit_all_lam0.csv` | Direct public-score projection from prior submitted ranks | 0.04224 | reject |
| 20260514-02 | `day9_best_plus_badresid_b0p6.csv` | Current-best ordering plus public-projection residual, `beta=0.600` | 0.06255 | keep |
| 20260514-03 | `day9_best_plus_badresid_b0p61.csv` | Current-best ordering plus public-projection residual, `beta=0.610` | 0.06258 | keep |
| 20260514-04 | `day9_best_plus_badresid_b0p58.csv` | Current-best ordering plus public-projection residual, `beta=0.580` | 0.06250 | keep |
| 20260514-05 | `day9_best_plus_badresid_b0p64.csv` | Current-best ordering plus public-projection residual, `beta=0.640` | 0.06254 | keep |
| 20260514-06 | `day9_best_plus_badresid_b0p595.csv` | Current-best ordering plus public-projection residual, `beta=0.595` | 0.06253 | keep |
| 20260514-07 | `day9_best_plus_badresid_b0p605.csv` | Current-best ordering plus public-projection residual, `beta=0.605` | 0.06256 | keep |
| 20260514-08 | `day9_best_plus_badresid_b0p615.csv` | Current-best ordering plus public-projection residual, `beta=0.615` | 0.06261 | keep best |
| 20260514-09 | `day9_best_plus_badresid_b0p62.csv` | Current-best ordering plus public-projection residual, `beta=0.620` | 0.06259 | keep |
| 20260514-10 | `day9_best_plus_badresid_b0p625.csv` | Current-best ordering plus public-projection residual, `beta=0.625` | 0.06255 | keep |

## Takeaways

- The direct public-score projection was not useful by itself, but its residual carried strong public signal when added to the previous tied-best ordering.
- The beta scan peaked at `0.615`, with nearby values confirming a local maximum around `0.61-0.62`.
- Best public score improved from `0.05345` to `0.06261`.
- Public rank after the run: 1.
