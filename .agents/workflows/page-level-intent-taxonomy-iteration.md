---
description: 
---

---
name: page-level-intent-taxonomy-iteration
description: Execute one complete taxonomy extraction, curation, approval, validation and persistence iteration.
---

# Execution Rules

This workflow is executed strictly in the order defined below.

Before Step 1 completes:

- Do not inspect project files.
- Do not search the repository.
- Do not access external URLs.
- Do not request tool permissions.
- Do not execute any skill.

The only permitted action before Step 1 completes is requesting the required user inputs.

After receiving the required inputs, execute one workflow step at a time.

Complete the current step before beginning the next.

Never skip, reorder, merge, or speculate about workflow steps.

If a step requires user input or approval, stop immediately and wait for the user's response before continuing.

---

# Workflow

## Required Inputs

- page_directory
- remote_address

The page directory contains all page-specific artifacts.

Expected structure:

page_directory/
├── source.md
├── taxonomy.md
├── curation.md
├── notes.md

File purposes:

- source.md — Input source page URL.
- taxonomy.md — Final approved taxonomy for the current page.
- curation.md — Append-only audit log for the current page.
- notes.md — Page-specific observations recorded during finalization.

---

## Step 1 — Collect Required Inputs

This is a blocking step.

The workflow MUST begin by collecting the required inputs.

Until Step 1 has completed successfully, do not:

- inspect the project workspace
- search the repository
- read project files
- access external URLs
- request tool permissions
- execute any workflow skill
- perform any workflow planning beyond requesting the required input

1. Request the page_directory from the user.

2. Wait for the user to provide the page_directory.

3. Do not assume, infer, or fabricate the page_directory.

4. Only after the page_directory has been provided:

   - Verify that the directory exists.
   - Verify that source.md, taxonomy.md, curation.md, and notes.md exist.
   - Read source.md.
   - Extract the source_url.
   - Determine the remote_address from mcp.json.

Do not execute any subsequent workflow step until Step 1 has completed successfully.

---

## Step 2 — Extract Candidate Intents

Execute Skill:

extract-candidate-intents-from-page

Inputs:

- source_url

Expected Output:

- PAGE_INTENT_CANDIDATES

---

## Step 3 — Persist Candidate Intents

Execute Skill:

write-with-git

Inputs:

- PAGE_INTENT_CANDIDATES
- page_directory/curation.md
- write_mode = APPEND

---

## Step 4 — Generate Taxonomy Change Proposals

Execute Skill:

review-candidate-intents-from-page

Inputs:

- source_url
- PAGE_INTENT_CANDIDATES

Expected Output:

- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE
- REVIEW_VALIDATION_CHECKS

---

## Step 5 — Persist User Approvals

Execute Skill:

write-with-git

Inputs:

- USER_APPROVAL_TABLE
- page_directory/curation.md
- write_mode = APPEND

---

## Step 6 — Finalize Taxonomy

Execute Skill:

finalise-intents-from-page

Inputs:

- PAGE_INTENT_CANDIDATES
- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE

Expected Output:

- PAGE_INTENT_FINAL

---

## Step 7 — Persist Final Taxonomy

Execute Skill:

write-with-git

Inputs:

- PAGE_INTENT_FINAL
- page_directory/taxonomy.md
- write_mode = WRITE

---

## Step 8 — Push Version History

Execute Skill:

write-with-git

Operation:

Execute the Push section from Skill write-with-git to push all local commits to the configured remote repository.

---

# Success Criteria

The workflow succeeds only if:

- Candidate intents were extracted.
- Change proposals were generated.
- Human approvals were collected.
- Final taxonomy was generated.
- Every write operation has been versioned.
- All commits have been successfully pushed.

---

# Failure Conditions

Stop immediately if:

- source page cannot be read
- intent extraction fails
- taxonomy review fails
- human approval is unavailable
- taxonomy validation fails
- file persistence fails
- git commit fails
- git push fails

Never continue after a failed stage.

Never bypass human approval.

Never fabricate evidence.

Never skip versioning after a successful write operation.