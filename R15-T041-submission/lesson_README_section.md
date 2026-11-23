## Applied lab — fictional spoken-timer security scenarios

Try the [R15-T041 security-scenario rubric](applied-labs/r15-t041/README.md), a **fictional, structure-only** example connected to spoken timer confirmation. It includes **Spoofed timer completion**, **Overheard timer feedback**, and **Changed timer duration**. Each has `asset`, `threat`, `control`, and `residual_risk` fields. All three fixture scenarios print `PASS`; a missing asset prints `FAIL`; an unrelated threat/control topic is flagged `REVIEW`, not rejected automatically. A human must judge whether each explanation and control is actually sound.

From the repository root, using only Python 3's standard library:

```sh
python3 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041/example.py
python3 -m unittest discover -s 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041 -p "test_*.py"
```

This is not a real timer, audio system, hardware test, cloud call, or security validation.

