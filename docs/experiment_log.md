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
| 20260507-01 | 2026-05-07 23:00 | Huber minus failed Ridge rank component, `t=0.18` | Fine grid below `t=0.24` | 0.05341 | keep best | Current best public score and leaderboard rank 1. |
| 20260507-02 | 2026-05-07 23:01 | Huber minus failed Ridge rank component, `t=0.20` | Fine grid below `t=0.24` | 0.05337 | keep | Above previous best, below `t=0.18`. |
| 20260507-03 | 2026-05-07 23:01 | Huber minus failed Ridge rank component, `t=0.21` | Fine grid below `t=0.24` | 0.05337 | keep | Similar to `t=0.20`. |
| 20260507-04 | 2026-05-07 23:02 | Huber minus failed Ridge rank component, `t=0.22` | Fine grid below `t=0.24` | 0.05336 | keep | Slightly below `t=0.20-0.21`. |
| 20260507-05 | 2026-05-07 23:02 | Huber minus failed Ridge rank component, `t=0.23` | Fine grid below `t=0.24` | 0.05334 | keep | Still above the former rank-1 score. |
| 20260507-06 | 2026-05-07 23:03 | Huber minus failed Ridge rank component, `t=0.25` | Fine grid above `t=0.24` | 0.05327 | reject | Correction is too strong. |
| 20260507-07 | 2026-05-07 23:03 | Huber minus failed Ridge rank component, `t=0.27` | Fine grid above `t=0.24` | 0.05325 | reject | Correction is too strong. |
| 20260507-08 | 2026-05-07 23:04 | Huber minus Ridge and ElasticNet rank components | Spearman with prior best `0.9994` | 0.05321 | reject | Extra component did not help. |
| 20260507-09 | 2026-05-07 23:04 | Apply `t=0.24` correction only to even-numbered codes | Code-group diagnostic | 0.05126 | reject | Code-filtered correction was harmful. |
| 20260507-10 | 2026-05-07 23:05 | Apply `t=0.24` correction only to high-count codes | Code-group diagnostic | 0.05124 | reject | Code-filtered correction was harmful. |
| 20260509-01 | 2026-05-09 20:47 | Huber minus failed Ridge rank component, `t=0.12` | Fine grid below `t=0.18` | 0.05316 | reject | Correction too weak. |
| 20260509-02 | 2026-05-09 20:47 | Huber minus failed Ridge rank component, `t=0.14` | Fine grid below `t=0.18` | 0.05329 | reject | Improved but below current best. |
| 20260509-03 | 2026-05-09 20:47 | Huber minus failed Ridge rank component, `t=0.15` | Fine grid below `t=0.18` | 0.05330 | reject | Improved but below current best. |
| 20260509-04 | 2026-05-09 20:48 | Huber minus failed Ridge rank component, `t=0.16` | Fine grid below `t=0.18` | 0.05342 | keep | Slightly above previous best. |
| 20260509-05 | 2026-05-09 20:49 | Huber minus failed Ridge rank component, `t=0.17` | Fine grid near `t=0.18` | 0.05342 | keep | Tied with `t=0.16`. |
| 20260509-06 | 2026-05-09 20:49 | Huber minus failed Ridge rank component, `t=0.175` | Fine grid near `t=0.18` | 0.05345 | keep best | Current best public score and leaderboard rank 1. |
| 20260509-07 | 2026-05-09 20:49 | Huber minus failed Ridge rank component, `t=0.185` | Fine grid near `t=0.18` | 0.05338 | reject | Slightly too much correction. |
| 20260509-08 | 2026-05-09 20:50 | Huber minus failed Ridge rank component, `t=0.19` | Fine grid above `t=0.18` | 0.05340 | reject | Below `t=0.175`. |
| 20260509-09 | 2026-05-09 20:51 | Huber minus clipped failed Ridge rank component, `t=0.18` | 1%-99% clipped component | 0.05342 | reject | Clipping did not beat plain `t=0.175`. |
| 20260509-10 | 2026-05-09 20:51 | Huber minus nonlinear failed Ridge rank component, `t=0.18` | Power transform diagnostic | 0.05341 | reject | Nonlinear transform did not improve. |
| 20260510-01 | 2026-05-10 00:32 | Huber minus failed Ridge rank component, `t=0.162` | Fine grid near `t=0.175` | 0.05342 | reject | Below current best. |
| 20260510-02 | 2026-05-10 00:32 | Huber minus failed Ridge rank component, `t=0.166` | Fine grid near `t=0.175` | 0.05341 | reject | Below current best. |
| 20260510-03 | 2026-05-10 00:32 | Huber minus failed Ridge rank component, `t=0.168` | Fine grid near `t=0.175` | 0.05342 | reject | Below current best. |
| 20260510-04 | 2026-05-10 00:33 | Huber minus failed Ridge rank component, `t=0.172` | Fine grid near `t=0.175` | 0.05343 | reject | Close, but below current best. |
| 20260510-05 | 2026-05-10 00:33 | Huber minus failed Ridge rank component, `t=0.174` | Fine grid near `t=0.175` | 0.05343 | reject | Close, but below current best. |
| 20260510-06 | 2026-05-10 00:34 | Huber minus failed Ridge rank component, `t=0.176` | Fine grid near `t=0.175` | 0.05344 | keep | Closest challenger to current best. |
| 20260510-07 | 2026-05-10 00:34 | Huber minus failed Ridge rank component, `t=0.178` | Fine grid near `t=0.175` | 0.05341 | reject | Correction slightly too strong. |
| 20260510-08 | 2026-05-10 00:35 | Huber minus failed Ridge rank component, `t=0.180` | Fine grid near `t=0.175` | 0.05341 | reject | Correction slightly too strong. |
| 20260510-09 | 2026-05-10 00:35 | Huber minus failed Ridge rank component, `t=0.182` | Fine grid near `t=0.175` | 0.05339 | reject | Correction too strong. |
| 20260510-10 | 2026-05-10 00:35 | Huber minus clipped failed Ridge rank component, `t=0.175` | 0.5%-99.5% clipped component | 0.05345 | keep | Tied current best; clipping did not improve. |
| 20260512-01 | 2026-05-12 07:59 | Huber minus failed Ridge rank component, `t=0.1745` | Very fine grid near `t=0.175` | 0.05344 | keep | Stable high score, just below current best. |
| 20260512-02 | 2026-05-12 08:00 | Huber minus failed Ridge rank component, `t=0.1755` | Very fine grid near `t=0.175` | 0.05345 | keep | Tied current best; no further lift. |
| 20260512-03 | 2026-05-12 08:00 | Huber minus failed Ridge rank component, `t=0.1765` | Very fine grid near `t=0.175` | 0.05344 | keep | Slightly below current best. |
| 20260512-04 | 2026-05-12 08:01 | Huber minus failed Ridge rank component, `t=0.1735` | Very fine grid near `t=0.175` | 0.05342 | reject | Weaker than the tighter peak candidates. |
| 20260512-05 | 2026-05-12 08:01 | Huber minus failed Ridge rank component, `t=0.1725` | Very fine grid near `t=0.175` | 0.05344 | keep | Stable but no improvement. |
| 20260512-06 | 2026-05-12 08:02 | Huber minus failed Ridge rank component, `t=0.1695` | Lower-side probe around the peak | 0.05342 | reject | Too little correction. |
| 20260512-07 | 2026-05-12 08:02 | Huber minus failed Ridge rank component, `t=0.1805` | Upper-side probe around the peak | 0.05341 | reject | Too much correction. |
| 20260512-08 | 2026-05-12 08:03 | Huber minus clipped failed Ridge rank component, `t=0.175` | 1%-99% clipped component | 0.05345 | keep | Tied current best; stronger clipping did not improve. |
| 20260512-09 | 2026-05-12 08:03 | Huber minus clipped failed Ridge rank component, `t=0.170` | 0.5%-99.5% clipped component | 0.05342 | reject | Clipped lower-side probe underperformed. |
| 20260512-10 | 2026-05-12 08:13 | Huber minus clipped failed Ridge rank component, `t=0.180` | 0.5%-99.5% clipped component | 0.05341 | reject | Clipped upper-side probe underperformed. |
