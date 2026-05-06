# Experiment Log

| ID | Date UTC | Hypothesis | Validation / Diagnostic | Public LB | Decision | Notes |
| --- | --- | --- | --- | ---: | --- | --- |
| setup | 2026-05-05 | Establish data profile and baseline | GroupKFold by `code`, baseline RankIC `0.04005` | 0.04387 | baseline | Initial known score. |
| 20260505-01 | 2026-05-05 09:26 | Blend official sample ordering with robust Huber ordering | Sample rank correlation `0.9896` | 0.04696 | reject | Better than baseline, worse than direct Huber. |
| 20260505-02 | 2026-05-05 09:26 | Robust Huber model on engineered numeric features | GroupKFold by `code` RankIC `0.04673` | 0.05220 | keep | Best result from first run. |
| 20260505-03 | 2026-05-05 09:27 | Blend official sample ordering with Ridge ordering | Sample rank correlation `0.9890` | 0.04628 | reject | Sample-preserving blend underperformed direct models. |
| 20260505-04 | 2026-05-05 09:27 | Ridge on engineered numeric features | GroupKFold by `code` RankIC `0.04322` | 0.04884 | reject | Useful but below Huber. |
| 20260505-05 | 2026-05-05 09:27 | ElasticNet on engineered numeric features | GroupKFold by `code` RankIC `0.04333` | 0.04843 | reject | Similar to Ridge, below Huber. |
| 20260505-06 | 2026-05-05 09:30 | Rank-normalized ElasticNet variant | GroupKFold by `code` RankIC `0.04783` | 0.02553 | reject | Local score did not transfer to leaderboard. |
| 20260505-07 | 2026-05-05 09:30 | Rank-normalized Ridge variant | GroupKFold by `code` RankIC `0.04757` | 0.02004 | reject | Same failure mode as previous row. |
| 20260505-08 | 2026-05-05 09:30 | Single-feature probe `-(f_0 - f_1)` | Train RankIC `0.04710` | 0.04231 | reject | Local single-feature signal did not transfer. |
| 20260505-09 | 2026-05-05 09:31 | Single-feature probe `-std(f_0,f_1,f_2,f_5,f_6)` | Train RankIC `0.04653` | 0.04099 | reject | Local single-feature signal did not transfer. |
| 20260505-10 | 2026-05-05 09:31 | Huber-centered rank ensemble | Spearman with Huber `0.9633` | 0.04814 | reject | Ensemble diluted the Huber ordering. |
| 20260506-01 | 2026-05-06 04:28 | Huber minus failed ElasticNet rank component, `t=0.35` | Spearman with Huber `0.9597` | 0.05271 | reject | Improved over Huber, below Ridge-component correction. |
| 20260506-02 | 2026-05-06 04:29 | Huber minus failed Ridge rank component, `t=0.28` | Spearman with Huber `0.9706` | 0.05329 | keep | Confirmed useful correction direction. |
| 20260506-03 | 2026-05-06 04:29 | Huber plus sample ordering, `t=0.30` | Spearman with Huber `0.9859` | 0.05208 | reject | Sample direction remained weak. |
| 20260506-04 | 2026-05-06 04:30 | Huber plus sample ordering, `t=0.15` | Spearman with Huber `0.9957` | 0.05226 | reject | Conservative sample direction remained weak. |
| 20260506-05 | 2026-05-06 04:31 | Huber minus failed Ridge rank component, `t=0.24` | Fine grid near `t=0.28` | 0.05332 | keep best | Current best public score. |
| 20260506-06 | 2026-05-06 04:32 | Huber minus failed Ridge rank component, `t=0.26` | Fine grid near `t=0.24` | 0.05328 | reject | Slightly below `t=0.24`. |
| 20260506-07 | 2026-05-06 04:32 | Huber minus failed Ridge rank component, `t=0.30` | Fine grid near `t=0.24` | 0.05321 | reject | Too much correction. |
| 20260506-08 | 2026-05-06 04:33 | Huber minus failed Ridge rank component, `t=0.32` | Fine grid near `t=0.24` | 0.05321 | reject | Too much correction. |
| 20260506-09 | 2026-05-06 04:34 | Huber minus failed Ridge rank component, `t=0.23` | Fine grid near `t=0.24` | 0.05252 | reject | Fine rank changes were not smooth on Public LB. |
| 20260506-10 | 2026-05-06 04:34 | Huber minus failed Ridge rank component, `t=0.25` | Fine grid near `t=0.24` | 0.05254 | reject | Fine rank changes were not smooth on Public LB. |
