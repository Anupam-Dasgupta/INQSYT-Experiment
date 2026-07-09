You are an expert intent taxonomist and customer service analyst specializing in e-commerce support.



Your task is to analyze an Amazon Customer Service help page, extract a comprehensive list of candidate customer intents, propose structural taxonomy changes, and generate a final verification checklist.



An "intent" represents the underlying customer goal (e.g., "return an item", "track a package").



ONLY extract the intents that are supported by this page. Do not extract the intents from the outside pages referred in this page.



### INPUT



Source Page URL: https://www.amazon.com/gp/help/customer/display.html?nodeId=GENAFPTNLHV7ZACW



### INSTRUCTIONS



Please read the file `Step 1 Plan.md` located in the root of this workspace. This file contains the overarching iteration workflow, the data dictionaries, and the exact Markdown schema you must use for your output tables.



**Phase 1: Generate Candidate Intents**
Carefully analyze the provided source page and identify every distinct customer goal addressed. Extract these into the `PAGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_INTENT\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CANDIDATES` format as defined in `Step 1 Plan.md`. Ensure every intent is grounded in the text with exact evidence spans, and that the intent names strictly follow a concise `verb\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_object` format.



**Phase 2: Generate Change Proposals**
Reflect critically on your initial list of candidate intents to propose taxonomy refinements. Document these in the `PAGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_INTENT\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CHANGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_PROPOSALS` format as defined in `Step 1 Plan.md`. Look for opportunities to split broad intents, merge overlapping intents, rename for clarity, or add/delete intents based on the source page.



**Phase 3: Generate Validation Checklist**
Output the `STEP\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_1\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CHECKS` table exactly as defined in `Step 1 Plan.md` for the human reviewer to approve.



### REQUIRED OUTPUT



Provide your findings as three Markdown tables (`PAGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_INTENT\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CANDIDATES`, `PAGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_INTENT\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CHANGE\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_PROPOSALS`, and `STEP\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_1\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\_CHECKS`), strictly matching the columns and schemas defined in your `Step 1 Plan.md` file.



### EXTRA COMMENTS



In addition to the required outputs, generate your observations on the following.



#### What is this page about?



Write a short summary describing what customer goals does this page support. You can give high level intent clusters that this page covers.



#### Intent Boundary Ambiguities



Give me your comments on intent boundary ambiguities observed on this page.



#### Chunking Hints



Give me your observations for the effective chunking of this page so that a RAG system is able to do a better retrieval.



### AFTER GENERATING OUTPUT



#### Human Approval for Change Proposal



Ask me one by one whether I want to approve the change proposals and at the end apply all the approved change proposals. Give me the final PAGE\_INTENT\_FINAL table.



When you are asking me for approval, show me the exact row from INTENT\_CHANGE\_PROPOSALS table that you want me to approve.



#### Human Approval for Intent Taxonomy Validation



After this, ask me one by one whether I approve the step 1 validation checks


### ADDITIONAL REQUIRED OUTPUT FILES

In addition to the required Markdown tables, you **MUST** generate and maintain the following three Markdown files throughout the execution of this task.

These files are considered mandatory outputs.

---

#### 1. `taxonomy.md`

This file represents the current state of the intent taxonomy extracted from this page.

It must contain:

- Source page URL
- Page title
- Short page summary
- Intent hierarchy (if any)
- Complete list of extracted candidate intents
- Final approved intent list
- Parent-child relationships (where applicable)
- Synonyms or alternate phrasings observed
- Duplicate or overlapping intents
- Intent naming rationale (where applicable)
- Final taxonomy after all approved change proposals have been applied

The taxonomy should always represent the **latest approved state** rather than the initial extraction.

---

#### 2. `curation.md`

This file serves as the complete working notebook for the taxonomy curation process.

It must record the intermediate work performed while building the taxonomy.

Include sections such as:

- Initial page observations
- Page understanding
- Intent extraction notes
- Supporting evidence collected for each intent
- Intent boundary discussions
- Candidate merge opportunities
- Candidate split opportunities
- Candidate rename discussions
- Deleted candidate intents and the reasons
- Added candidate intents and the reasons
- Every taxonomy change proposal
- Human approvals and rejections
- Final curation decisions
- Validation notes
- Any assumptions made during extraction

This file should function as a complete audit trail explaining how the taxonomy evolved from the source page to the final approved taxonomy.

**Do not overwrite or delete previous reasoning.** Instead, append updates chronologically as the taxonomy evolves.

---

#### 3. `notes.md`

This file contains observations that are useful for future taxonomy curation but do not belong inside the taxonomy itself.

Examples include:

- General observations about the page
- Navigation structure
- Page quality observations
- Missing documentation
- Missing intents that may exist elsewhere but are intentionally excluded
- Retrieval challenges
- RAG chunking recommendations
- Intent ambiguity observations
- Reusable extraction patterns
- Taxonomy design observations
- Future cleanup opportunities
- Edge cases noticed during extraction
- Any other information that may help future human curators

This file is intentionally free-form.

---

### FILE MAINTENANCE REQUIREMENTS

Treat all three Markdown files as **living documents** throughout the task.

Whenever new information becomes available:

- Immediately update `taxonomy.md` if the taxonomy changes.
- Append new reasoning to `curation.md`.
- Append useful observations to `notes.md`.

Do **not** wait until the end of the task to construct these files.

At every stage, these files should accurately reflect the current state of the work.

---

### CONSISTENCY REQUIREMENTS

Before producing the final answer, perform a consistency verification.

Verify that:

- Every intent appearing in `PAGE_INTENT_FINAL` exists in `taxonomy.md`.
- Every approved taxonomy change has been applied to `taxonomy.md`.
- Every approved or rejected change proposal is recorded in `curation.md`.
- Every important observation discussed during the task has been captured in `notes.md`.
- Every intent in the taxonomy has supporting evidence from the source page.
- No unsupported external intents have been introduced.
- The final taxonomy is internally consistent with the generated Markdown tables.

If any inconsistency is detected, resolve it before generating the final output.

---

### FINAL DELIVERABLES

At the conclusion of the task, output the complete contents of the following files as separate Markdown sections:

1. `taxonomy.md`
2. `curation.md`
3. `notes.md`

These files must be complete, self-contained, and understandable without requiring access to the conversation history.

The contents of `taxonomy.md` must exactly match the final approved intent taxonomy.

