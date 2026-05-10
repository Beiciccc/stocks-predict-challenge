# Submission Summary 2026-05-10

Competition: `stocks-challenge`

Requested submissions: 10

Completed submissions: 10

All submitted files passed local schema, ID-order, NaN, and inf checks before submission. Kaggle accepted each file, each produced a new submissions-list record, and each reached `SubmissionStatus.COMPLETE` with a public score.

| ID | Description | Public Score |
| --- | --- | ---: |
| 20260510-01 | Huber minus failed Ridge rank component, `t=0.162` | 0.05342 |
| 20260510-02 | Huber minus failed Ridge rank component, `t=0.166` | 0.05341 |
| 20260510-03 | Huber minus failed Ridge rank component, `t=0.168` | 0.05342 |
| 20260510-04 | Huber minus failed Ridge rank component, `t=0.172` | 0.05343 |
| 20260510-05 | Huber minus failed Ridge rank component, `t=0.174` | 0.05343 |
| 20260510-06 | Huber minus failed Ridge rank component, `t=0.176` | 0.05344 |
| 20260510-07 | Huber minus failed Ridge rank component, `t=0.178` | 0.05341 |
| 20260510-08 | Huber minus failed Ridge rank component, `t=0.180` | 0.05341 |
| 20260510-09 | Huber minus failed Ridge rank component, `t=0.182` | 0.05339 |
| 20260510-10 | Huber minus clipped failed Ridge rank component, `t=0.175` | 0.05345 |

Best submission remains `t=0.175` Ridge-component correction, public score `0.05345`.

Leaderboard after run: public best `0.05345`, rank 1 of 17 shown teams.

## Conclusions

- The `t=0.175` correction remains the best confirmed setting.
- The closest new challenger was `t=0.176` at `0.05344`.
- Slightly lower settings (`0.162-0.174`) and higher settings (`0.178-0.182`) did not improve.
- Clipping the correction component tied the current best but did not exceed it.
