---
name: taxonomy-extraction
description: Extract candidate customer intents and supporting evidence from a customer support page.
---

# Purpose

Extract every customer intent that is explicitly supported by the supplied page.

Generate only the initial taxonomy.

Do not refine or approve it.

---

# Inputs

- Source page URL
- Source page content
- Step 1 specification

---

# Outputs

- PAGE_INTENT_CANDIDATES table

---

# Responsibilities

- Read the source page.
- Identify every customer goal supported by the page.
- Name intents using the verb_object convention.
- Ground every intent using exact evidence.
- Do not invent unsupported intents.

---

# Must Not

- Approve taxonomy changes.
- Modify taxonomy.md.
- Validate outputs.
- Merge or delete intents unless explicitly requested.

---

# References

templates/step1_plan.md