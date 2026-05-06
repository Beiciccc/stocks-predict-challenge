# Submission Summary 2026-05-06

Competition: `stocks-challenge`

Requested submissions: 10

Completed submissions: 10

All submitted files passed local schema, ID-order, NaN, and inf checks before submission. Kaggle accepted each file, each produced a new submissions-list record, and each reached `SubmissionStatus.COMPLETE` with a public score.

| ID | Description | Public Score |
| --- | --- | ---: |
| 20260506-01 | Huber minus failed ElasticNet rank component, `t=0.35` | 0.05271 |
| 20260506-02 | Huber minus failed Ridge rank component, `t=0.28` | 0.05329 |
| 20260506-03 | Huber plus sample ordering, `t=0.30` | 0.05208 |
| 20260506-04 | Huber plus sample ordering, `t=0.15` | 0.05226 |
| 20260506-05 | Huber minus failed Ridge rank component, `t=0.24` | 0.05332 |
| 20260506-06 | Huber minus failed Ridge rank component, `t=0.26` | 0.05328 |
| 20260506-07 | Huber minus failed Ridge rank component, `t=0.30` | 0.05321 |
| 20260506-08 | Huber minus failed Ridge rank component, `t=0.32` | 0.05321 |
| 20260506-09 | Huber minus failed Ridge rank component, `t=0.23` | 0.05252 |
| 20260506-10 | Huber minus failed Ridge rank component, `t=0.25` | 0.05254 |

Best submission: `t=0.24` Ridge-component correction, public score `0.05332`.

Leaderboard after run: public best `0.05332`, rank 2 of 17 shown teams.

## Conclusions

- Removing a small amount of a failed Ridge rank component from the Huber baseline is the strongest confirmed direction.
- Best observed correction is `huber - 0.24 * ridge_rank_component` after rank normalization.
- Larger corrections (`0.30`, `0.32`) fall back to `0.05321`.
- Sample-submission blending remains worse than the Huber correction.
- The next useful work is careful analysis of the `t=0.24` rank changes rather than broad new model families.
