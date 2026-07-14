---
description: 
---

---
name: page-level-chunk-generation-iteration
description: Execute one complete semantic chunk generation, curation, approval, validation and persistence iteration.
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
├── chunks.md
├── curation.md
├── notes.md

File purposes:

- source.md — Input source page URL.
- taxonomy.md — Final approved taxonomy for the current page.
- chunks.md — Final approved semantic chunking for the current page.
- curation.md — Append-only audit log for the current page.
- notes.md — Semantic observations that assist future retrieval and corpus-wide taxonomy consolidation.

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

4. Verify that the supplied page_directory exists.

5. Verify that source.md exists inside the page_directory.

6. Verify that taxonomy.md exists inside the page_directory.

7. If source.md or taxonomy.md does not exist, stop immediately.

8. If chunks.md does not exist:

   - create an empty markdown file named chunks.md
   - do not overwrite an existing file
   - do not write any initial content

9. Read source.md.

10. Extract the source_url.

11. Read taxonomy.md.

12. Extract PAGE_INTENT_FINAL.

13. Determine the remote_address from mcp.json.

Proceed only after all required inputs have been collected and validated.

Do not execute any subsequent workflow step until Step 1 has completed successfully.

---

## Step 2 — Generate Candidate Chunks

Execute Skill:

generate-chunking-recommendations

Inputs:

- source_url
- PAGE_INTENT_FINAL

Expected Output:

- PAGE_CHUNK_CANDIDATES
- PAGE_CHUNK_CHANGE_PROPOSALS
- USER_APPROVAL_CHUNK_TABLE
- CHUNKING_VALIDATION_CHECKS

---

## Step 3 — Persist User Approvals

Execute Skill:

write-with-git

Inputs:

- USER_APPROVAL_CHUNK_TABLE
- page_directory/curation.md
- write_mode = APPEND

---

## Step 4 — Persist Final Chunking

Execute Skill:

write-with-git

Inputs:

- PAGE_CHUNK_FINAL
- page_directory/chunks.md
- write_mode = WRITE

---

## Step 5 — Push Version History

Execute Skill:

write-with-git

Operation:

Execute the Push section from Skill write-with-git to push all local commits to the configured remote repository.

---

# Success Criteria

The workflow succeeds only if:

- Candidate chunks were generated.
- Chunk refinement proposals were generated.
- Human approvals were collected.
- Final chunking was generated.
- Every write operation has been versioned.
- All commits have been successfully pushed.

---

# Failure Conditions

Stop immediately if:

- source page cannot be read
- taxonomy cannot be read
- chunk generation fails
- human approval is unavailable
- chunk validation fails
- file persistence fails
- git commit fails
- git push fails

Never continue after a failed stage.

Never bypass human approval.

Never fabricate chunk boundaries.

Never fabricate supporting evidence.

Never skip versioning after a successful write operation.