---
name: write-with-git
description: Persist project outputs and create a Git version after every successful write operation.
---

# Purpose

Persist project artifacts to the specified destination.

Version every successful write operation using Git.

This skill performs persistence and versioning only.
It does not modify the supplied content.

---

# Preconditions

The following must be available:

- Content
- Destination file
- write_mode
- A valid Git repository

Stop immediately if any prerequisite cannot be satisfied.

---

# Inputs

- Content
- Destination file
- write_mode

Allowed write modes:

- WRITE
  Overwrite the destination file.

- APPEND
  Append the supplied content to the destination file.

---

# Procedure

1. If write_mode is WRITE, overwrite the destination file with the supplied content.

2. If write_mode is APPEND, append the supplied content to the destination file.

3. Verify that the write operation completed successfully.

4. Stage only the files modified by this write operation.

5. Generate an appropriate commit message describing the logical change.

6. Ask the user for confirmation before committing if required by the active workflow.

7. Create exactly one Git commit representing this logical write operation.

8. Report:

- write status
- modified files
- commit hash
- commit message

---

# Validation

Verify that:

- write_mode is WRITE or APPEND
- the destination file exists before APPEND
- the write operation completed successfully
- only intended files were modified
- the Git commit was created successfully

---

# Push

When instructed by the active workflow:

1. Push all local commits to the configured remote repository.

2. Verify that the push completed successfully.

3. Report:

- push status
- remote branch

---

# Constraints

Never:

- use force push
- rewrite history
- commit unrelated files
- commit secrets
- ignore write failures

---

# Output

Return:

- write status
- modified files
- commit message
- commit hash
- push status (if executed)

---

# Failure Conditions

Stop immediately if:

- the write operation fails
- Git staging fails
- Git commit fails
- Git push fails

Never silently ignore failures.
Never continue after a failed write or versioning operation.

---

# Success Criteria

The skill succeeds only if:

- the requested write operation completed successfully
- the correct files were staged
- exactly one Git commit was created
- all validation checks pass