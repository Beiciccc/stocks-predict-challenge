# Submission Summary - 2026-05-12

## Context

- Competition metadata checked before submission: rules remain unchanged, metric remains RankIC, and the public data files remain the same.
- Starting best public score: `0.05345`.
- Starting public rank: 1.
- Experiment focus: very fine threshold probes around the current best `t=0.175`, plus clipped variants on both sides of the peak.

## Results

| ID | File | Description | Public LB | Decision |
| --- | --- | --- | ---: | --- |
| 20260512-01 | `day6_corr_t01745.csv` | Huber minus failed Ridge rank component, `t=0.1745` | 0.05344 | keep |
| 20260512-02 | `day6_corr_t01755.csv` | Huber minus failed Ridge rank component, `t=0.1755` | 0.05345 | keep |
| 20260512-03 | `day6_corr_t01765.csv` | Huber minus failed Ridge rank component, `t=0.1765` | 0.05344 | keep |
| 20260512-04 | `day6_corr_t01735.csv` | Huber minus failed Ridge rank component, `t=0.1735` | 0.05342 | reject |
| 20260512-05 | `day6_corr_t01725.csv` | Huber minus failed Ridge rank component, `t=0.1725` | 0.05344 | keep |
| 20260512-06 | `day6_corr_t01695.csv` | Huber minus failed Ridge rank component, `t=0.1695` | 0.05342 | reject |
| 20260512-07 | `day6_corr_t01805.csv` | Huber minus failed Ridge rank component, `t=0.1805` | 0.05341 | reject |
| 20260512-08 | `day6_corr_t0175_clip01.csv` | Huber minus clipped failed Ridge rank component, `t=0.175` | 0.05345 | keep |
| 20260512-09 | `day6_corr_t0170_clip005.csv` | Huber minus clipped failed Ridge rank component, `t=0.170` | 0.05342 | reject |
| 20260512-10 | `day6_corr_t0180_clip005.csv` | Huber minus clipped failed Ridge rank component, `t=0.180` | 0.05341 | reject |

## Takeaways

- The public score peak remains narrow around `t=0.175`.
- `t=0.1755` and clipped `t=0.175` tied the current best but did not improve it.
- Both lower-side and upper-side clipped probes underperformed, so clipping does not appear to be the next useful direction.
- Best public score remains `0.05345`; public rank remains 1 after this run.
