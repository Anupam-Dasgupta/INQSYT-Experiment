---
name: extract-candidate-intents-from-page
description: Extract grounded candidate customer intents from a single support page.
---

# Purpose

Extract every customer intent supported by the supplied source page.

This skill performs only candidate intent extraction.

It does NOT:

- propose taxonomy changes
- finalize taxonomy
- apply approvals

---

# Preconditions

The following must be available:

- source_url
- specification/intent-taxonomy-context.md

Stop immediately if either cannot be accessed.

---

# Inputs

- Source page URL

---

# Required References

Before execution read:

- specification/intent-taxonomy-context.md

These specifications define:

- extraction methodology
- naming conventions
- required markdown schemas
- evidence requirements
- validation requirements

They are the authoritative source.

---

# Procedure

1. Read the source page.

2. Identify every distinct customer goal explicitly supported by the page.

3. Extract every supported customer intent.

4. Follow the required verb_object naming convention.

5. Ground every intent using exact evidence from the page.

6. Do not invent intents.

7. Ignore external pages referenced by the page.

8. Produce the PAGE_INTENT_CANDIDATES table exactly as defined by the intent-taxonomy-context.md file.

9. Present the completed PAGE_INTENT_CANDIDATES table to the user exactly as defined by the specification.

10. Do not summarize, abbreviate, or omit rows from the table.

11. Displaying PAGE_INTENT_CANDIDATES is informational only.

12. After presenting the table, immediately return PAGE_INTENT_CANDIDATES to the calling workflow.

13. Do not pause execution after displaying the table unless explicitly instructed by the calling workflow.

---

# Output

- Present PAGE_INTENT_CANDIDATES to the user.
- Return PAGE_INTENT_CANDIDATES to the calling workflow.

---

# Validation

Before completion verify:

- every intent has evidence
- naming convention is correct
- schema exactly matches specification
- no unsupported intents exist

---

# Success Criteria

The skill succeeds only if:

- PAGE_INTENT_CANDIDATES has been produced
- every candidate intent is evidence-grounded
- every supported customer goal has been captured
- all validation checks pass

---

# Failure Conditions

Stop immediately if:

- source page cannot be read
- evidence is insufficient
- schema cannot be satisfied

Never fabricate information.