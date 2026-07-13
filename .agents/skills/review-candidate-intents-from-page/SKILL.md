---
name: review-candidate-intents-from-page
description: Generate taxonomy refinement proposals from candidate intents.
---

# Purpose

Review the extracted candidate intents against the existing taxonomy.

Generate taxonomy refinement proposals where appropriate.

This skill proposes changes only.

It never modifies the taxonomy or assumes human approval.

---

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

Review the extracted intents.

Identify only evidence-supported opportunities to:

- ADD
- MERGE
- SPLIT
- RENAME
- DELETE

Do not generate a proposal unless it provides a clear improvement to the taxonomy.

Every proposal must:

- be supported by page evidence
- contain clear reasoning
- use the required schema

Present PAGE_INTENT_CHANGE_PROPOSALS to the user.

Request explicit approval or rejection for every proposal.

Record every decision in USER_APPROVAL_TABLE.

Do not continue until every proposal has been explicitly marked as APPROVED or REJECTED.

Do not modify the taxonomy.
Do not assume approval.

Produce:

REVIEW_VALIDATION_CHECKS

---

# Output

- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE
- REVIEW_VALIDATION_CHECKS

---

# Constraints

Never:

- modify the taxonomy
- modify curation history
- assume human approval
- fabricate justification
- fabricate supporting evidence
- omit supported refinement opportunities

---

# Validation

Verify:

- every proposal has justification
- every proposal has evidence
- every proposal references one or more candidate intents
- no duplicate proposals exist
- REVIEW_VALIDATION_CHECKS is complete

---

# Success Criteria

The skill succeeds only if:

- every refinement proposal is evidence-supported
- every proposal has an explicit human decision
- USER_APPROVAL_TABLE is complete
- REVIEW_VALIDATION_CHECKS is complete