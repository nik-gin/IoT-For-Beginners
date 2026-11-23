## Applied lab: R15-T050 — Geofence applied assessment

This **fictional local teaching example** extends this lesson with [geofence applied assessment](applied-labs/r15-t050/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 3-transport/lessons/1-location-tracking/applied-labs/r15-t050/example.py
python3 -m unittest discover -s 3-transport/lessons/1-location-tracking/applied-labs/r15-t050 -p "test_*.py"
```

Expected fixture/results: `(15,75) -> inside`, `(10,70) -> inside`, `(21,75) -> outside`, invalid latitude `100` rejected.

**Scope:** Inclusive rectangle only; not spherical distance or GPS observation. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

