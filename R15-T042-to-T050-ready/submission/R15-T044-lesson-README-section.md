## Applied lab: R15-T044 — Sensor-message state trace

This **fictional local teaching example** extends this lesson with [sensor-message state trace](applied-labs/r15-t044/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 1-getting-started/lessons/1-introduction-to-iot/applied-labs/r15-t044/example.py
python3 -m unittest discover -s 1-getting-started/lessons/1-introduction-to-iot/applied-labs/r15-t044 -p "test_*.py"
```

Expected fixture/results: `A@2`, `A@1`, duplicate `A@1`, invalid reading -> sorted `A@1,A@2`; rejected indices 2 and 3.

**Scope:** No real IoT device, message transport or cloud service is exercised. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

