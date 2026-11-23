## Applied lab: R15-T045 — Offline message-source adapter

This **fictional local teaching example** extends this lesson with [offline message-source adapter](applied-labs/r15-t045/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 6-consumer/lessons/1-speech-recognition/applied-labs/r15-t045/example.py
python3 -m unittest discover -s 6-consumer/lessons/1-speech-recognition/applied-labs/r15-t045 -p "test_*.py"
```

Expected fixture/results: Local callable returns `A@2`, `A@1`, duplicate `A@1`, invalid reading; accepts sorted `A@1,A@2`, rejects the last two.

**Scope:** The callable does not simulate real speech transcription, timing or service reliability. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

