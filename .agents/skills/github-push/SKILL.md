---

name: github-push
description: Safely commit and push approved project changes to GitHub.
---

# Purpose

Safely create a single, atomic Git commit containing only user-approved project changes and push it to the configured GitHub remote.

This skill exists to ensure that every commit is intentional, reviewable, reproducible, and free of unrelated modifications.

---

# When to Use

Use this skill whenever a logical unit of work has been completed and the user requests that the changes be committed or pushed to GitHub.

Do not use this skill for incomplete work or experimental changes.

---

# Inputs

The following information must be available before execution:

* Files approved for commit
* Repository location
* Branch to push
* Commit message (or permission to generate one)

---

# Preconditions

Before proceeding, verify that:

* The current directory is a Git repository.
* A Git remote is configured.
* The working tree is accessible.
* The approved files exist.
* The repository is in a valid state for committing.

If any precondition fails, stop and report the issue.

---

# Procedure

1. Determine the current repository.
2. Determine the active branch.
3. Run `git status`.
4. Review all modified, deleted, and untracked files.
5. Stage **only** the approved files.
6. Verify the staged changes using `git diff --cached`.
7. Ensure no unrelated files are staged.
8. Create a single atomic commit.
9. Push the commit to the configured remote.
10. Verify that the push completed successfully.

---

# Validation

Before creating the commit, verify that:

* Every staged file is approved.
* No unrelated files are staged.
* The commit represents exactly one logical change.
* No temporary or generated files have been included accidentally.

If validation fails, stop and explain why.

---

# Outputs

Upon successful completion, report:

* Repository
* Branch
* Remote
* Commit hash
* Commit message
* Files committed
* Push status

---

# Failure Conditions

Stop immediately if:

* The repository is invalid.
* Git reports merge conflicts.
* The push is rejected.
* An approved file cannot be found.
* Unapproved files would be committed.
* The repository requires user intervention.

Never attempt to work around failures automatically.

---

# Constraints

Never use:

* `git add .`
* `git add -A`

Never commit:

* temporary files
* caches
* logs
* build artifacts
* virtual environments
* secrets
* credentials
* datasets

unless the user explicitly approves them.

Never rewrite Git history.

Never force push unless explicitly instructed.

Never guess which files should be committed.

When uncertain, ask the user.

Always prefer safety over automation.

