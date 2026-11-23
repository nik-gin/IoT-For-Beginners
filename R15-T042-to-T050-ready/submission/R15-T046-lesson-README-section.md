## Applied lab: R15-T046 — Schema-validation refactor

This **fictional local teaching example** extends this lesson with [schema-validation refactor](applied-labs/r15-t046/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 1-getting-started/lessons/3-sensors-and-actuators/applied-labs/r15-t046/example.py
python3 -m unittest discover -s 1-getting-started/lessons/3-sensors-and-actuators/applied-labs/r15-t046 -p "test_*.py"
```

Expected fixture/results: Before and after both return `accepted=[A@1,A@2] rejected=[2:duplicate_device_timestamp,3:invalid_reading]` and `equal=true`.

**Scope:** A validation refactor over fictional JSON, not real sensor measurements. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

