---
name: finalise-intents-from-page
description: Apply approved taxonomy changes, generate the final taxonomy, and maintain structured project documentation.
---

# Purpose

Apply only the taxonomy changes explicitly approved by the human reviewer.

Generate the final approved taxonomy while preserving the complete audit trail and maintaining project documentation.

---

# Inputs

- PAGE_INTENT_CANDIDATES
- PAGE_INTENT_CHANGE_PROPOSALS
- Human approvals

---

# Required References

Read:

- specification/intent-taxonomy-context.md

---

# Procedure

## 1. Apply Taxonomy Changes

Apply **only** approved taxonomy changes.

Ignore every rejected proposal.

For every approved MERGE, create the proposed broader super-intent and preserve each merged source intent as a sub-intent. A MERGE must not delete or erase the merged intents from the taxonomy hierarchy.

Update:

- taxonomy.md

---

## 2. Update Curation History

Append a new entry to:

- curation.md

The curation history must include:

- Approved proposals
- Rejected proposals
- Intent merges
- Intent deletions
- Intent renames
- Human reasoning (when available)

Never rewrite previous curation history.

---

## 3. Update `notes.md`

Append a new iteration to `notes.md`.

The file must preserve all previous content and maintain the exact structure shown below.

Do **not** invent new headings.

Do **not** remove existing headings.

Do **not** overwrite previous iterations.

Use the following template exactly.

# Notes

## General Observations About the Page

Summarize:

- what the page primarily covers
- overall purpose
- notable documentation characteristics

---

## Navigation Structure

Describe:

- page sections
- navigation flow
- major workflows
- logical organization

---

## Page Quality Observations

Record observations such as:

- clarity
- duplication
- inconsistencies
- redirects
- formatting quality
- readability
- documentation quality

---

## Missing Documentation

Record important information that appears missing or insufficiently explained.

---

## Missing Intents (Intentionally Excluded)

List user intents that may appear related but should **not** become taxonomy intents.

Include a brief explanation for each exclusion.

---

## Retrieval Challenges

Describe any retrieval difficulties, including:

- mixed topics
- overlapping concepts
- scattered information
- long workflows
- retrieval ambiguity
- embedding challenges

---

## RAG Chunking Recommendations

Recommend logical chunk boundaries for retrieval.

Each recommendation should preserve semantic meaning while maximizing retrieval quality.

---

## Intent Ambiguity Observations

Describe situations where:

- multiple intents overlap
- terminology is ambiguous
- similar user requests could map to different intents

---

## Reusable Extraction Patterns

Record reusable linguistic patterns such as:

- conditional wording
- fallback wording
- approval language
- redirect language
- common documentation styles
- recurring extraction cues

These observations should help improve future extraction.

---

## Taxonomy Design Observations

Document:

- naming decisions
- intent merges
- taxonomy simplifications
- structural improvements
- normalization decisions

---

## Edge Cases Noticed During Extraction

Document unusual situations such as:

- asynchronous workflows
- human approvals
- exception paths
- conditional behavior
- uncommon business rules

---

## Iteration <N> - Observations (<DATE>)

Append a new iteration only.

Each iteration should summarize:

- important extraction observations
- approved taxonomy changes
- rejected taxonomy changes
- retrieval observations
- taxonomy decisions
- chunking observations
- notable edge cases
- lessons useful for future pages

Never modify previous iterations.

Always append the new iteration beneath the existing ones.

---

## 4. Verify Consistency

After updating all files, verify that every approved taxonomy change has been reflected consistently across:

- taxonomy.md
- curation.md
- notes.md

---

## Generate

Generate:

- PAGE_INTENT_FINAL

`PAGE_INTENT_FINAL` must use the schema defined in `specification/intent-taxonomy-context.md`:

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|

Generation rules:

- Emit one row for every final intent relationship.
- For an approved MERGE, set `intent_name` to the new super-intent and `sub-intent` to one preserved merged intent.
- Emit one row per preserved sub-intent.
- For an intent with no sub-intent, leave `sub-intent` empty.
- Never output only the super-intent when approved merged sub-intents exist.

---

# Validation

Verify that:

### Taxonomy

- Every final intent exists in `taxonomy.md`.
- Every approved MERGE has one super-intent and all of its preserved sub-intents represented.
- No approved merged intent has been discarded or omitted.
- Every `PAGE_INTENT_FINAL` row conforms to the five-column schema, including the `sub-intent` column immediately after `intent_name`.
- Intents without sub-intents have an empty `sub-intent` cell.
- No rejected proposal has been applied.
- Every approved proposal has been applied exactly once.

### Curation

- Every approval is recorded.
- Every rejection is recorded.
- Previous curation history has been preserved.
- New decisions have been appended rather than replacing existing history.

### Notes

Verify that:

- `notes.md` still contains all previous iterations.
- A new iteration has been appended.
- The required headings appear exactly as specified.
- No headings have been renamed.
- No previous notes have been deleted.
- Previous iterations remain unchanged.
- The document structure matches the established template.

---

# Constraints

Never apply rejected proposals.

Never implement MERGE as destructive replacement of the merged intents.

Never omit approved sub-intents from `PAGE_INTENT_FINAL` or `taxonomy.md`.

Never overwrite:

- taxonomy history
- curation history
- notes history

Always append.

Never rewrite previous iterations.

Never invent additional headings in `notes.md`.

Always preserve the established `notes.md` structure.

---

# Output

Generate:

- PAGE_INTENT_FINAL

Updated files:

- taxonomy.md
- curation.md
- notes.md