# Strict GitHub Push Instructions

You must follow these instructions exactly.



## Objective

Push **only** the changes explicitly specified by the user to the correct GitHub repository.

\---



## Before Doing Anything

1. Determine the current Git repository.
2. Verify the active branch.
3. Run `git status`.
4. Review all modified, deleted, and untracked files.
5. Do **not** stage or commit anything until you have verified the files to be included.

\---



## Strict Rules

* Stage **only** the files listed in **Files to Push**.
* Do **not** use `git add .`.
* Do **not** use `git add -A`.
* Do **not** use wildcard staging unless it is explicitly requested.
* Do **not** include unrelated modifications.
* Do **not** include temporary files, logs, caches, datasets, virtual environments, or generated artifacts unless explicitly requested.
* If any listed file does not exist, stop and report it.
* If there are unstaged changes outside the approved list, leave them untouched.

\---



## Files to Push

\---



## Commit

Write a concise, descriptive commit message based only on the approved changes.

\---



## Verification

Before pushing:

1. Run `git diff --cached`.
2. Verify that **every staged file** appears in the approved list.
3. Verify that **no unapproved file** is staged.

If there is any mismatch, stop and report it.

\---



## Push

Push the commit to the current branch's configured remote.

\---



## Final Report

Report:

* Repository
* Branch
* Commit hash
* Commit message
* Files committed
* Push status

Do not claim success unless the push completed successfully.

