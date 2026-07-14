---
name: generate-chunking-recommendations
description: Generate candidate semantic chunks for the approved page taxonomy and propose chunking refinements.
---

# Purpose

Generate semantic candidate chunks for every intent in the approved page taxonomy.

Review the generated chunks and propose chunking refinements where appropriate.

This skill proposes chunking changes only.

It never finalizes chunks or assumes human approval.

---

# Preconditions

The following must be available:

- source_url
- PAGE_INTENT_FINAL
- specification/intent-taxonomy-context.md

Stop immediately if any required input cannot be read.

---

# Inputs

- Source page URL
- PAGE_INTENT_FINAL

---

# Required References

Read:

- specification/intent-taxonomy-context.md

---

# Procedure

Read the source page.

Read PAGE_INTENT_FINAL.

For every intent in PAGE_INTENT_FINAL:

- Identify all supporting content.
- Generate one or more candidate semantic chunks.
- Preserve the source text exactly as it appears.
- Never paraphrase, rewrite, summarize, or modify the source text.
- Candidate chunks must consist of contiguous spans copied directly from the source page.
- Every chunk must support one or more approved intents.
- Preserve logical semantic boundaries.
- Do not split coherent procedures unless necessary.
- Do not combine unrelated customer goals into a single chunk.
- Include a chunk_boundary_justification explaining why the selected text forms a distinct semantic unit and why it should remain separate from adjacent content.

Produce PAGE_CHUNK_CANDIDATES.

Review the generated candidate chunks.

Identify only evidence-supported opportunities to:

- ADD
- DELETE
- MERGE
- SPLIT
- MODIFY
- REASSIGN

Do not generate a proposal unless it clearly improves chunk quality, retrieval quality, or semantic coherence.

Every proposal must:

- be supported by page evidence
- contain clear reasoning
- reference one or more candidate chunks
- use the required schema

Present PAGE_CHUNK_CHANGE_PROPOSALS to the user.

Request explicit approval or rejection for every proposal.

Record every decision in USER_APPROVAL_CHUNK_TABLE.

Do not continue until every proposal has been explicitly marked as APPROVED or REJECTED.

Do not finalize chunking.

Produce:

CHUNKING_VALIDATION_CHECKS

---

# Output

- PAGE_CHUNK_CANDIDATES
- PAGE_CHUNK_CHANGE_PROPOSALS
- USER_APPROVAL_CHUNK_TABLE
- CHUNKING_VALIDATION_CHECKS

---

# Constraints

Never:

- modify PAGE_INTENT_FINAL
- assume human approval
- fabricate chunk boundaries
- fabricate supporting evidence
- omit supported chunking opportunities
- create chunks unsupported by the page
- create chunks for external pages

---

# Validation

Verify:

- every approved intent is supported by at least one candidate chunk
- every chunk has supporting evidence
- every proposal has justification
- every proposal has evidence
- every proposal references one or more candidate chunks
- no duplicate proposals exist
- every proposal has an explicit human decision
- CHUNKING_VALIDATION_CHECKS is complete

---

# Success Criteria

The skill succeeds only if:

- PAGE_CHUNK_CANDIDATES has been generated
- every approved intent is represented by one or more chunks
- every chunk is evidence-supported
- every refinement proposal is evidence-supported
- every proposal has an explicit human decision
- USER_APPROVAL_CHUNK_TABLE is complete
- CHUNKING_VALIDATION_CHECKS is complete

---

# Failure Conditions

Stop immediately if:

- source page cannot be read
- PAGE_INTENT_FINAL is unavailable
- chunk generation fails
- evidence is insufficient
- human approval is unavailable

Never fabricate chunk boundaries.

Never fabricate supporting evidence.

Never continue after a failed stage.