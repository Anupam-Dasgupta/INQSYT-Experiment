---
name: review-candidate-intents-from-page
description: Critically review extracted candidate intents and generate evidence-supported taxonomy refinement proposals.
---

# Purpose

You are a taxonomy critic.

Your job is to critically review the extracted candidate intents in PAGE_INTENT_CANDIDATES.

Assume the extracted intents are a draft that may contain:

- unsupported intents
- duplicate intents
- overlapping intents
- inconsistent naming
- inconsistent granularity
- missing customer goals

Your objective is to improve the quality, consistency, and maintainability of the taxonomy.

Challenge the extracted candidate intents rather than accepting them at face value.

Prefer improving existing candidate intents through:

- DELETE
- MERGE
- SPLIT
- RENAME

Only propose ADD when an explicit customer goal supported by the page cannot be represented by any existing candidate intent.

This skill proposes taxonomy refinements only.

It never modifies the taxonomy or assumes human approval.

# Preconditions

The following must be available:

- source_url
- PAGE_INTENT_CANDIDATES
- specification/intent-taxonomy-context.md

Stop immediately if any required input cannot be read.

---

# Inputs

- Source page URL
- PAGE_INTENT_CANDIDATES

---

# Required References

Read:

- specification/intent-taxonomy-context.md

---

# Procedure

## Phase 1 — Review Individual Candidate Intents

Review every extracted candidate intent independently.

For every candidate intent evaluate:

- Is the intent explicitly supported by the source page?
- Does the intent represent exactly one customer goal?
- Is the intent name clear, precise, and consistent with the required naming convention?
- Is the scope appropriately granular?
- Is the intent too broad?
- Is the intent too narrow?
- Does the evidence fully support the intent?

If any issue is identified, record the appropriate refinement opportunity.

Do not generate proposals yet.

---

## Phase 2 — Review Relationships Between Candidate Intents

Compare every candidate intent against every other candidate intent.

Identify opportunities where:

- two intents describe the same customer goal
- one intent completely contains another
- multiple intents should be merged
- one intent should be split into multiple independent customer goals
- naming conventions are inconsistent
- intent boundaries overlap
- customer goals are represented at inconsistent levels of abstraction

Do not generate proposals yet.

---

## Phase 3 — Review Coverage

Review the page as a whole.

Determine whether every customer goal explicitly supported by the page has been represented.

Only if a supported customer goal is missing from PAGE_INTENT_CANDIDATES should an ADD proposal be considered.

Do not invent customer goals.

Do not infer unsupported intents.

---

## Phase 4 — Generate Taxonomy Change Proposals

Generate proposals only where they clearly improve:

- semantic precision
- taxonomy consistency
- customer goal separation
- retrieval quality
- long-term maintainability

Evaluate proposal types in the following order:

1. DELETE unsupported intents.
2. MERGE duplicate or substantially overlapping intents.
3. SPLIT intents representing multiple independent customer goals.
4. RENAME unclear or inconsistent intent names.
5. ADD missing evidence-supported intents.

Do not generate a proposal unless it provides a clear improvement over the current candidate taxonomy.

Every proposal must:

- reference one or more candidate intents
- contain supporting evidence
- contain clear reasoning
- identify the proposal type
- follow the required schema defined in intent-taxonomy-context.md

Multiple proposal types may reference the same candidate intent if justified.

---

## Phase 5 — Human Approval

Present PAGE_INTENT_CHANGE_PROPOSALS.

Request explicit approval or rejection for every proposal.

Record every decision in USER_APPROVAL_TABLE.

Do not continue until every proposal has been explicitly marked as APPROVED or REJECTED.

Do not modify the taxonomy.

Do not assume approval.

---

## Phase 6 — Construct Final Intent Table

After all proposals receive human decisions, construct FINAL_INTENT_TABLE.

Columns:

- intent
- description
- source_chunks
- subintents

### Rules

**Approved MERGE**
- Retain the approved super intent.
- Every merged-away intent becomes a subintent.

**Approved DELETE**
- Deleted intent names are attached as subintents of the retained canonical intent whose semantics best represent them.

**Rejected ADD**
- Do not create a new canonical intent.
- Attach the rejected intent name as a subintent of the closest retained canonical intent.

**Dropped / Non-retained Candidate Intents**
- Any candidate intent that does not become a canonical intent, but whose semantics are represented by a retained canonical intent, must be stored as a subintent.

**Approved RENAME**
- Replace the canonical name.
- Do not create a subintent unless explicitly required by downstream systems.

**Approved SPLIT**
- Each resulting intent becomes an independent canonical intent.
- No subintents are created solely because of a split.

**Empty Subintents**
- If none exist, use:
  ```yaml
  subintents: []
  ```

### Invariants

- Every intent name must appear exactly once in the final taxonomy.
- An intent name must appear either:
  - as a canonical intent, OR
  - as a subintent.
- No subintent may belong to multiple canonical intents.
- Canonical intent names must never appear inside subintents.

---

## Phase 7 — Validation

Produce:

REVIEW_VALIDATION_CHECKS

Verify:

- every candidate intent has been individually reviewed
- every candidate intent has been compared against all other candidates
- the entire page has been reviewed for missing customer goals
- every proposal is evidence-supported
- every proposal has clear reasoning
- every proposal references one or more candidate intents
- no duplicate proposals exist
- USER_APPROVAL_TABLE is complete
- FINAL_INTENT_TABLE is complete
- every approved merge contributes subintents
- every rejected ADD is preserved as a subintent
- every approved DELETE is preserved as a subintent
- every non-retained intent appears exactly once as a subintent
- no duplicate subintents exist

---

# Output

- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE
- FINAL_INTENT_TABLE
- REVIEW_VALIDATION_CHECKS

---

# Constraints

Never:

- modify the taxonomy
- modify curation history
- assume human approval
- fabricate evidence
- fabricate justification
- invent unsupported customer goals
- generate proposals solely to increase the number of intents
- prefer ADD proposals over other proposal types

Prefer improving existing candidate intents through:

- DELETE
- MERGE
- SPLIT
- RENAME

Only propose ADD when an explicit customer goal supported by the page cannot be represented by any existing candidate intent.

---

# Success Criteria

The skill succeeds only if:

- every candidate intent has been critically reviewed
- every refinement proposal is evidence-supported
- proposal types appropriately include DELETE, MERGE, SPLIT, RENAME, and ADD where justified
- every proposal has an explicit human decision
- USER_APPROVAL_TABLE is complete
- FINAL_INTENT_TABLE is complete
- every merged intent is preserved as a subintent
- every rejected ADD is preserved as a subintent
- every deleted/non-retained intent is preserved as a subintent
- no duplicate subintents exist
- REVIEW_VALIDATION_CHECKS is complete

---

# Failure Conditions

Stop immediately if:

- source page cannot be read
- PAGE_INTENT_CANDIDATES cannot be read
- evidence is insufficient
- human approval is unavailable

Never fabricate taxonomy refinements.

Never continue after a failed stage.
