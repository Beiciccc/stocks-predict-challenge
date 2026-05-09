# Submission Summary 2026-05-09

Competition: `stocks-challenge`

Requested submissions: 10

Completed submissions: 10

All submitted files passed local schema, ID-order, NaN, and inf checks before submission. Kaggle accepted each file, each produced a new submissions-list record, and each reached `SubmissionStatus.COMPLETE` with a public score.

| ID | Description | Public Score |
| --- | --- | ---: |
| 20260509-01 | Huber minus failed Ridge rank component, `t=0.12` | 0.05316 |
| 20260509-02 | Huber minus failed Ridge rank component, `t=0.14` | 0.05329 |
| 20260509-03 | Huber minus failed Ridge rank component, `t=0.15` | 0.05330 |
| 20260509-04 | Huber minus failed Ridge rank component, `t=0.16` | 0.05342 |
| 20260509-05 | Huber minus failed Ridge rank component, `t=0.17` | 0.05342 |
| 20260509-06 | Huber minus failed Ridge rank component, `t=0.175` | 0.05345 |
| 20260509-07 | Huber minus failed Ridge rank component, `t=0.185` | 0.05338 |
| 20260509-08 | Huber minus failed Ridge rank component, `t=0.19` | 0.05340 |
| 20260509-09 | Huber minus clipped failed Ridge rank component, `t=0.18` | 0.05342 |
| 20260509-10 | Huber minus nonlinear failed Ridge rank component, `t=0.18` | 0.05341 |

Best submission: `t=0.175` Ridge-component correction, public score `0.05345`.

Leaderboard after run: public best `0.05345`, rank 1 of 17 shown teams.

## Conclusions

- The best correction coefficient moved from `t=0.18` to `t=0.175`.
- The useful region is narrow: `t=0.16`, `0.17`, `0.175`, and clipped `0.18` are close, but `0.12` and `0.185+` are weaker.
- Clipping and nonlinear transforms did not improve over the plain rank component.
