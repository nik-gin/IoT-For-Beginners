## Applied lab: R15-T049 — Edge security scenario recovery

This **fictional local teaching example** extends this lesson with [edge security scenario recovery](applied-labs/r15-t049/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 4-manufacturing/lessons/3-run-fruit-detector-edge/applied-labs/r15-t049/example.py
python3 -m unittest discover -s 4-manufacturing/lessons/3-run-fruit-detector-edge/applied-labs/r15-t049 -p "test_*.py"
```

Expected fixture/results: Three fictional complete scenarios -> `PASS`; missing asset -> `FAIL`; next complete input -> `PASS`; unrelated tags -> `REVIEW`.

**Scope:** Structure-only checks; human judges security correctness. No model/device used. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

