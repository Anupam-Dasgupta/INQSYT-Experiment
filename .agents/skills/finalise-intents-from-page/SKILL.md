---
name: finalise-intents-from-page
description: Apply approved taxonomy changes and generate the final taxonomy.
---

# Purpose

Apply only human-approved taxonomy changes.

Generate the final approved page intents.

Update the taxonomy, curation history, and notes to reflect the approved changes.

---

# Preconditions

The following must be available:

- PAGE_INTENT_CANDIDATES
- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE
- taxonomy.md
- curation.md
- specification/intent-taxonomy-context.md

Stop immediately if any required input cannot be read.

---

# Inputs

- PAGE_INTENT_CANDIDATES
- PAGE_INTENT_CHANGE_PROPOSALS
- USER_APPROVAL_TABLE

---

# Required References

Read:

- specification/intent-taxonomy-context.md

---

# Procedure

1. Read PAGE_INTENT_CANDIDATES.

2. Read PAGE_INTENT_CHANGE_PROPOSALS.

3. Read USER_APPROVAL_TABLE.

4. Apply only the proposals marked APPROVED.

5. Ignore every proposal marked REJECTED.

6. Update taxonomy.md to reflect the approved changes.

7. Append the approval decisions to curation.md.

8. Append observations to notes.md that may assist future chunk generation, retrieval, and corpus-wide taxonomy consolidation.

Examples include:

- page summary
- primary customer goals
- semantic section boundaries
- chunking recommendations
- retrieval challenges
- navigation structure
- intent boundary ambiguities
- terminology inconsistencies
- reusable extraction patterns
- documentation quality observations
- future taxonomy cleanup opportunities
- edge cases

Do not record:

- workflow events
- approval decisions
- rejected proposals
- accepted proposals
- audit history

These belong exclusively in curation.md.

9. Verify consistency between the updated taxonomy and the approved proposals.

10. Produce PAGE_INTENT_FINAL.

---

# Validation

Verify:

- every approved proposal has been applied
- no rejected proposal has been applied
- every final intent exists in taxonomy.md
- every approval and rejection has been recorded in curation.md
- notes.md contains any important observations
- PAGE_INTENT_FINAL matches the updated taxonomy

---

# Constraints

Never:

- apply rejected proposals
- assume approval
- modify previous curation history
- overwrite audit history
- fabricate taxonomy changes
- fabricate notes or observations

Always append new entries to curation.md.
Always preserve the complete audit history.

---

# Output

- PAGE_INTENT_FINAL

Updated:

- taxonomy.md
- curation.md
- notes.md

---

# Success Criteria

The skill succeeds only if:

- PAGE_INTENT_FINAL has been generated
- every approved proposal has been applied
- every rejected proposal has been ignored
- taxonomy.md is internally consistent
- curation.md has been updated
- all validation checks pass