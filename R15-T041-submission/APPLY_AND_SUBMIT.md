# Apply R15-T041 to your actual checkout

This delivery was built and tested in an isolated workspace because the real S-AI-Projects Git checkout was not mounted here, and the shell has no GitHub connectivity. **No real repository commit, push, PR or issue comment was made.** The supplied patch is the PR-sized change: exactly 3 added files and one lesson README insertion.

1. Copy `R15-T041.patch` and `PR_BODY.md` from this package somewhere accessible to your checkout. Verify the checkout is clean.
2. From the **real checkout**, using the task's assigned working branch as the starting point (or your instructor's specified base):

```sh
git status --short
git fetch origin
git switch student/e26b07f0724
git switch -c R15-T041
git apply --check /path/to/R15-T041.patch
git apply /path/to/R15-T041.patch
python3 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041/example.py
python3 -m unittest discover -s 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041 -p "test_*.py"
```

If `student/e26b07f0724` is only a remote branch, first use `git switch --track origin/student/e26b07f0724` instead. If branch `R15-T041` already exists, inspect it rather than blindly recreating it.

3. The intentionally failing run should exit 1; save that result in local `work/R15-T041/` if you rerun the task's checks:

```sh
R15_T041_NEGATIVE_TEST=1 python3 -m unittest discover -s 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041 -p "test_*.py"
```

4. Stage **only the four task files**, not `work/`:

```sh
git add 6-consumer/lessons/3-spoken-feedback/README.md
git add 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041/README.md
git add 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041/example.py
git add 6-consumer/lessons/3-spoken-feedback/applied-labs/r15-t041/test_example.py
git diff --cached --stat
git commit -m "Add fictional spoken-timer security rubric example (R15-T041)"
git push -u origin R15-T041
```

5. Open a PR whose **base repository is `S-AI-Projects/IoT-For-Beginners`**, **not** `microsoft/IoT-For-Beginners`. Check the correct base branch (normally `main`, unless instructor specified another) and verify the diff contains only the four named files. If GitHub CLI is installed/authenticated:

```sh
gh pr create --repo S-AI-Projects/IoT-For-Beginners --base main --head R15-T041 --title "R15-T041: fictional security-scenario rubric for spoken feedback" --body-file /path/to/PR_BODY.md
```

6. Post the resulting *real PR URL* as a comment on issue #5 and request the instructor's review using their actual GitHub handle. Do not invent a reviewer handle. Use GitHub UI if `gh` is not installed.

Note: The patch's README insertion was checked against a local matching heading stub; it **has not** been applied to the actual repository in this environment. `git apply --check` above is the definitive verification for your checkout. The task issue pins upstream reference commit `6ae558ee2b0aaade53f08b0f76505d5ea9736c43`; the actual pinned file content could not be downloaded into this workspace, so the current public fork lesson was consulted as a reference instead.
