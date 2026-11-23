# R15-T042 through R15-T050 — prepared offline changes

Each task has a standalone `example.py`, `test_example.py`, lab README, lesson README insertion patch, and actual test evidence under `work/R15-TXXX/`. Patches contain ONLY the three new lab files and a brief lesson README section, never work evidence.

| Task | GitHub issue | Tests run | Normal | Wrong expected result |
|---|---|---:|---|---|
| R15-T042 | [#43](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/43) | 6 | exit 0 | exit 1 (expected) |
| R15-T043 | [#44](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/44) | 5 | exit 0 | exit 1 (expected) |
| R15-T044 | [#45](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/45) | 7 | exit 0 | exit 1 (expected) |
| R15-T045 | [#46](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/46) | 9 | exit 0 | exit 1 (expected) |
| R15-T046 | [#47](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/47) | 7 | exit 0 | exit 1 (expected) |
| R15-T047 | [#48](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/48) | 7 | exit 0 | exit 1 (expected) |
| R15-T048 | [#49](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/49) | 8 | exit 0 | exit 1 (expected) |
| R15-T049 | [#50](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/50) | 6 | exit 0 | exit 1 (expected) |
| R15-T050 | [#51](https://github.com/S-AI-Projects/IoT-For-Beginners/issues/51) | 6 | exit 0 | exit 1 (expected) |

No PRs have been opened. The connected GitHub identity has read access but **no push permission** on the organisation fork. Use each `submission/R15-TXXX.patch` separately in a clean checkout, verify it with `git apply --check`, run its exact test command, and commit to an independent `R15-TXXX` branch. Push only when your account has write access or you are using your own fork; target **S-AI-Projects/IoT-For-Beginners** for PRs when instructed. Keep `work/` evidence out of submitted changes.
