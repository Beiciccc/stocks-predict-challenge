# Submission Summary 2026-05-05

Competition: `stocks-challenge`

Requested submissions: 10

Completed submissions: 10

All submitted files passed local schema, ID-order, NaN, and inf checks before submission. Kaggle accepted each file, each produced a new submissions-list record, and each reached `SubmissionStatus.COMPLETE` with a public score.

| ID | Description | Public Score |
| --- | --- | ---: |
| 20260505-01 | Sample + Huber blend | 0.04696 |
| 20260505-02 | Huber features | 0.05220 |
| 20260505-03 | Sample + Ridge blend | 0.04628 |
| 20260505-04 | Ridge features | 0.04884 |
| 20260505-05 | ElasticNet features | 0.04843 |
| 20260505-06 | Rank-normalized ElasticNet variant | 0.02553 |
| 20260505-07 | Rank-normalized Ridge variant | 0.02004 |
| 20260505-08 | Single-feature spread probe | 0.04231 |
| 20260505-09 | Single-feature volatility probe | 0.04099 |
| 20260505-10 | Huber-centered rank ensemble | 0.04814 |

Best submission: Huber features, public score `0.05220`.

Leaderboard after run: public best `0.05220`, rank 4 of 16 shown teams.

## Conclusions

- The direct robust Huber ordering was the strongest approach.
- Official-sample blends improved over the old baseline but diluted the Huber signal.
- Rank-normalized variants and single-feature probes did not transfer well to the public leaderboard.
- Future experiments should refine Huber-like robust regression and small rank perturbations around the Huber ordering.
