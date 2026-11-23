## Summary

Closes the runnable concept portion of S-AI-Projects/IoT-For-Beginners#5 (R15-T041).

- Adds three clearly labeled **fictional** spoken-timer security scenarios: Spoofed timer completion, Overheard timer feedback, and Changed timer duration.
- Encodes each with four fields: `asset`, `threat`, `control`, `residual_risk`.
- Adds a Python 3 standard-library **structure-only** checker: `PASS` for complete fixtures with matching author-provided topic tags, `FAIL` for missing or blank required fields, and `REVIEW` for mismatched threat/control tags (human judgment required).
- Adds unittest coverage, an opt-in intentionally incorrect assertion, lab documentation, and a link from the spoken-feedback lesson.

No hardware, audio generation, cloud API, model download, pip dependencies, or real security claims.

## Checks

From the repository root:

```sh
python3 -m unittest discover -s 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041 -p "test_*.py"
```

Actual local result (Python 3.13.5): **Ran 7 tests; OK (skipped=1); exit 0**. The skip is the opt-in negative canary.

```sh
R15_T041_NEGATIVE_TEST=1 python3 -m unittest discover -s 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041 -p "test_*.py"
```

Actual local result: **Ran 7 tests; FAILED (failures=1); exit 1**. This is **expected**: the canary incorrectly asserts that a valid scenario has status `FAIL`.

The local evidence logs are in `work/R15-T041/` and are **not part of this PR**.

Please review the lesson fit and scenario/control explanations: the automated checker does **not** grade their correctness.
