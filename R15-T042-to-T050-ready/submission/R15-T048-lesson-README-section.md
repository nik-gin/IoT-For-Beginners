## Applied lab: R15-T048 — Three-size message evaluation

This **fictional local teaching example** extends this lesson with [three-size message evaluation](applied-labs/r15-t048/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 6-consumer/lessons/1-speech-recognition/applied-labs/r15-t048/example.py
python3 -m unittest discover -s 6-consumer/lessons/1-speech-recognition/applied-labs/r15-t048 -p "test_*.py"
```

Expected fixture/results: 4/8/16 input records -> accepted 2/4/8 and rejected 2/4/8; `acceptance_fraction=0.50` for each.

**Scope:** Counts only; no model accuracy, timing or production throughput claim. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

