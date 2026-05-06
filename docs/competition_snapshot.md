# Competition Snapshot

Snapshot date: 2026-05-06

## Description

The task is to predict `y` for anonymized stock features. Stock codes are represented by `code`; features are `f_0` through `f_6`.

The competition states that different stocks are used in the training and test sets. There is no overlap between train/test stock codes, and no overlap between public/private leaderboard stock codes. This makes cross-stock generalization the central validation problem.

## Evaluation

Kaggle page content: `We use RankIC.`

Local validation records therefore use rank correlation / Spearman-style checks, with grouping by `code` where applicable.

## Rules

Kaggle page content: `Have fun!`
