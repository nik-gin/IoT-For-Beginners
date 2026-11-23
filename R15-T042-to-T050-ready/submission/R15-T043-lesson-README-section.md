## Applied lab: R15-T043 — Geofence membership comparison

This **fictional local teaching example** extends this lesson with [geofence membership comparison](applied-labs/r15-t043/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 3-transport/lessons/4-geofences/applied-labs/r15-t043/example.py
python3 -m unittest discover -s 3-transport/lessons/4-geofences/applied-labs/r15-t043 -p "test_*.py"
```

Expected fixture/results: `(15,75)` and boundary `(10,70)` -> `inside`; `(21,75)` -> `outside`; `(100,75)` -> rejected invalid latitude.

**Scope:** Inclusive rectangle only, not spherical distance, polygon or live GPS. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

