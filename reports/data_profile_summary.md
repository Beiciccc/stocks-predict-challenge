# Data Profile Summary

Snapshot date: 2026-05-06

| File | Rows | Columns |
| --- | ---: | ---: |
| `train.csv` | 15,767 | 10 |
| `test.csv` | 34,233 | 9 |
| `sample_submission.csv` | 34,233 | 2 |

## Columns

- Train: `id`, `code`, `f_0`, `f_1`, `f_2`, `f_3`, `f_4`, `f_5`, `f_6`, `y`
- Test: `id`, `code`, `f_0`, `f_1`, `f_2`, `f_3`, `f_4`, `f_5`, `f_6`
- Submission: `id`, `y`

## Split Facts

- Train IDs: `0` to `15766`.
- Test IDs: `15767` to `49999`.
- Train stock codes: 14 unique values.
- Test stock codes: 28 unique values.
- Train/test code overlap: 0.

## Notes

- The target `y` has mean about `-0.2851` and standard deviation about `0.4186` in train.
- `f_3` has extreme test values not present in train, so robust modeling or clipping diagnostics are important.
- Official sample submission values are not constant and have nontrivial rank structure.
