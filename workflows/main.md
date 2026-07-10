# Workflow: Main

## Goal

Execute one complete taxonomy curation iteration from source page analysis through Git versioning.

This workflow coordinates the project skills. Individual skills are responsible for their own implementation details.

---

# Inputs

- Source page URL
- User instructions
- Project workspace
- Existing project state

---

# Workflow

## Step 1 — Load Context

- Read the user's request.
- Determine the target source page.
- Load any existing project state if available.
- Verify that the required project files exist.

---

## Step 2 — Execute Taxonomy Extraction

Execute Skill:

.ai/skills/taxonomy-extraction/SKILL.md

Expected Output:

- PAGE_INTENT_CANDIDATES

---

## Step 3 — Execute Taxonomy Curation

Execute Skill:

.ai/skills/taxonomy-curation/SKILL.md

Expected Output:

- PAGE_INTENT_CHANGE_PROPOSALS
- Updated taxonomy.md
- Updated curation.md

---

## Step 4 — Human Review

Present every taxonomy change proposal.

Wait for the user's approval or rejection.

No taxonomy changes may be finalized without explicit approval.

---

## Step 5 — Execute Taxonomy Validation

Execute Skill:

.ai/skills/taxonomy-validation/SKILL.md

Expected Output:

- STEP_1_CHECKS
- Final PAGE_INTENT_FINAL
- Updated taxonomy.md
- Updated curation.md
- Updated notes.md

---

## Step 6 — Final Review

Present the final deliverables.

Verify that:

- all required outputs exist
- all validation checks pass
- project state is internally consistent

---

## Step 7 — Git Versioning

If the user requests version control:

Execute Skill:

.ai/skills/github-push/SKILL.md

---

# Success Criteria

The workflow is complete only if:

- Candidate intents have been extracted.
- Change proposals have been generated.
- Human approvals have been incorporated.
- Validation succeeds.
- Project state has been updated.
- Git versioning completes successfully (when requested).

---

# Failure Conditions

Stop execution if:

- the source page cannot be accessed
- extraction fails
- validation fails
- required files are missing
- human approval is required
- the GitHub Push skill reports failure

Never skip a workflow stage.

Never bypass human approval.

Never duplicate logic that belongs inside a Skill.