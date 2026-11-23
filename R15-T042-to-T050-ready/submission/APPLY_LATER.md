# Apply later (no PR created by this bundle)

Clone or open your existing checkout of `S-AI-Projects/IoT-For-Beginners`.
Each patch should be applied independently on a clean branch, not accumulated into one PR:

```sh
# From the root of your existing checkout:
git status --short  # check that there are no unrelated changes
git switch main     # or your designated base branch from the issue
git pull --ff-only

git switch -c R15-T042
git apply --check /path/to/R15-remaining-tasks/submission/R15-T042.patch
git apply /path/to/R15-remaining-tasks/submission/R15-T042.patch
python3 -m unittest discover -s 2-farm/lessons/3-automated-plant-watering/applied-labs/r15-t042 -p "test_*.py"
git add 2-farm/lessons/3-automated-plant-watering/README.md 2-farm/lessons/3-automated-plant-watering/applied-labs/r15-t042/
git commit -m "docs(lab): add R15-T042 moisture hysteresis boundaries"
# Do not push/open PR until you're ready.
```

Repeat for tasks T043–T050 using their specific patch, lesson path and test command. Never commit `work/` evidence to the PR. Inspect `git diff --cached` before committing. If a README context has changed since it was read, apply the corresponding `submission/R15-TXXX-lesson-README-section.md` immediately before the lesson's `## Assignment` heading manually and review the diff.

The issue specifies a working base branch `student/e26b07f0724`; use that branch instead of `main` if it exists and is your designated base. All nine patches were prepared against the observed `S-AI-Projects` fork lesson README endings, so verify `git apply --check` in your checkout.
