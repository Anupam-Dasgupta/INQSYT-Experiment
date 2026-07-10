---
name: taxonomy-validation
description: Validate that the taxonomy and supporting artifacts are internally consistent.
---

# Purpose

Verify that the generated taxonomy is complete, evidence-backed, and internally consistent.

---

# Inputs

- PAGE_INTENT_CANDIDATES
- PAGE_INTENT_CHANGE_PROPOSALS
- taxonomy.md
- curation.md
- notes.md

---

# Outputs

- STEP_1_CHECKS
- Validation report

---

# Responsibilities

Verify:

- every intent has evidence
- every approved change has been applied
- taxonomy.md matches the final taxonomy
- curation.md contains all decisions
- notes.md contains important observations

---

# Must Not

- Generate new intents.
- Modify the taxonomy.
- Skip failed validation.

---

# References

templates/step1_plan.md

state/taxonomy.md

state/curation.md

state/notes.md