## Applied lab: R15-T047 — Worked sensor-message regression

This **fictional local teaching example** extends this lesson with [worked sensor-message regression](applied-labs/r15-t047/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 4-manufacturing/lessons/2-check-fruit-from-device/applied-labs/r15-t047/example.py
python3 -m unittest discover -s 4-manufacturing/lessons/2-check-fruit-from-device/applied-labs/r15-t047 -p "test_*.py"
```

Expected fixture/results: Input `A@2`, `A@1`, duplicate `A@1`, invalid string reading -> accept, accept, reject, reject; sorted `A@1,A@2`.

**Scope:** Does not classify fruit images or measure a model. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

