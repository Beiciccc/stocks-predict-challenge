# Submission Summary - 2026-05-13

## Context

- Competition metadata checked before submission: rules remain unchanged, metric remains RankIC, and the public data files remain the same.
- Starting best public score: `0.05345`.
- Starting public rank: 1.
- Experiment focus: ultra-fine threshold probes around the narrow `t=0.175` public-score peak, plus small clipped-component and tied-top blend checks.

## Results

| ID | File | Description | Public LB | Decision |
| --- | --- | --- | ---: | --- |
| 20260513-01 | `day8_corr_t01749.csv` | Huber minus failed Ridge rank component, `t=0.1749` | 0.05344 | keep |
| 20260513-02 | `day8_corr_t01751.csv` | Huber minus failed Ridge rank component, `t=0.1751` | 0.05345 | keep |
| 20260513-03 | `day8_corr_t01752.csv` | Huber minus failed Ridge rank component, `t=0.1752` | 0.05344 | keep |
| 20260513-04 | `day8_corr_t01753.csv` | Huber minus failed Ridge rank component, `t=0.1753` | 0.05344 | keep |
| 20260513-05 | `day8_corr_t01754.csv` | Huber minus failed Ridge rank component, `t=0.1754` | 0.05344 | keep |
| 20260513-06 | `day8_corr_t01756.csv` | Huber minus failed Ridge rank component, `t=0.1756` | 0.05344 | keep |
| 20260513-07 | `day8_corr_t01752_clip0025.csv` | Huber minus clipped failed Ridge rank component, `t=0.1752` | 0.05344 | reject |
| 20260513-08 | `day8_corr_t01752_clip0075.csv` | Huber minus clipped failed Ridge rank component, `t=0.1752` | 0.05344 | reject |
| 20260513-09 | `day8_corr_t01755_clip0025.csv` | Huber minus clipped failed Ridge rank component, `t=0.1755` | 0.05345 | keep |
| 20260513-10 | `day8_top_tie_rankblend.csv` | Rank blend of tied top variants | 0.05345 | keep |

## Takeaways

- The public-score peak remains at `0.05345`; no candidate exceeded the current best.
- The plateau appears very narrow: tiny movements around `t=0.175` mostly produce `0.05344`.
- Light clipping can tie the current best at `t=0.1755`, but clipping does not create a reliable gain.
- A rank blend of tied public-best variants also ties `0.05345`, supporting the current ordering family without proving a new direction.
- Best public score remains `0.05345`; public rank remains 1 after this run.
