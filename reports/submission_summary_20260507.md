# Submission Summary 2026-05-07

Competition: `stocks-challenge`

Requested submissions: 10

Completed submissions: 10

All submitted files passed local schema, ID-order, NaN, and inf checks before submission. Kaggle accepted each file, each produced a new submissions-list record, and each reached `SubmissionStatus.COMPLETE` with a public score.

| ID | Description | Public Score |
| --- | --- | ---: |
| 20260507-01 | Huber minus failed Ridge rank component, `t=0.18` | 0.05341 |
| 20260507-02 | Huber minus failed Ridge rank component, `t=0.20` | 0.05337 |
| 20260507-03 | Huber minus failed Ridge rank component, `t=0.21` | 0.05337 |
| 20260507-04 | Huber minus failed Ridge rank component, `t=0.22` | 0.05336 |
| 20260507-05 | Huber minus failed Ridge rank component, `t=0.23` | 0.05334 |
| 20260507-06 | Huber minus failed Ridge rank component, `t=0.25` | 0.05327 |
| 20260507-07 | Huber minus failed Ridge rank component, `t=0.27` | 0.05325 |
| 20260507-08 | Huber minus Ridge and ElasticNet rank components | 0.05321 |
| 20260507-09 | `t=0.24` correction only on even-numbered codes | 0.05126 |
| 20260507-10 | `t=0.24` correction only on high-count codes | 0.05124 |

Best submission: `t=0.18` Ridge-component correction, public score `0.05341`.

Leaderboard after run: public best `0.05341`, rank 1 of 17 shown teams.

## Conclusions

- The best correction moved from `t=0.24` to `t=0.18`.
- Scores declined gradually from `t=0.18` through `t=0.27`, suggesting the useful correction is smaller than the prior best coefficient.
- Adding an ElasticNet rank component did not help.
- Applying the correction only to selected code groups was harmful.
