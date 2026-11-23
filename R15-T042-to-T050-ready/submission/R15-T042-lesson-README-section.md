## Applied lab: R15-T042 — Moisture-control hysteresis

This **fictional local teaching example** extends this lesson with [moisture-control hysteresis](applied-labs/r15-t042/README.md). Requires only Python 3 (standard library); no device, service, subscription or downloads.

Run from the repository root:

```sh
python3 2-farm/lessons/3-automated-plant-watering/applied-labs/r15-t042/example.py
python3 -m unittest discover -s 2-farm/lessons/3-automated-plant-watering/applied-labs/r15-t042 -p "test_*.py"
```

Expected fixture/results: `[700,250,400,650]` starting off -> `off,on,on,off`; readings `300`/`600` retain state, invalid `1024` rejected.

**Scope:** Does not control or test a real relay, pump or moisture sensor. The lab README explains boundaries, invalid cases and how to demonstrate a deliberately failing assertion.

