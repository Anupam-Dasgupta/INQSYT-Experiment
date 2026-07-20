### CONTEXT: ITERATION WORKFLOW

#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|\[Source URL]|\[verb\_object]|\[One-sentence description of the customer goal]|\[Exact text span from the source page]|


#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change\_type|change\_instruction|change\_reason|change\_evidence|is\_approved|
|-|-|-|-|-|-|
|\[Source URL]|\[MERGE / SPLIT / RENAME / ADD / DELETE]|\[Short, precise description of the proposed change]|\[Reason why the change is recommended]|\[Exact text span supporting the change, if applicable]|No|


#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|[Source URL]|[MERGE / SPLIT / RENAME / ADD / DELETE]|[Short, precise description of the proposed change]|[Reason why the change is recommended]|[Exact text span supporting the change, if applicable]|[APPROVED / REJECTED]|


#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|No|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|No|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|No|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|No|


#### PAGE_INTENT_FINAL

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|[Source URL]|[verb_object]|[verb_object or empty]|[One-sentence description of the customer goal represented by this row]|[Exact text span from the source page]|

For an approved MERGE, preserve the merged intents as sub-intents beneath the new super-intent. Emit one row per super-intent/sub-intent relationship.

Example:

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|[Source URL]|manage_account|edit_address|Manage account information, including address changes.|[Exact supporting text span]|
|[Source URL]|manage_account|edit_name|Manage account information, including name changes.|[Exact supporting text span]|
|[Source URL]|request_lawyer||Request assistance from a lawyer.|[Exact supporting text span]|

If an intent has no sub-intent, leave the `sub-intent` cell empty.


#### PAGE_CHUNK_CANDIDATES

|url|chunk_id|supported_intents|candidate_chunk|chunk_boundary_justification|evidence|
|-|-|-|-|-|-|
|[Source URL]|[chunk_name]|[Comma-separated approved intent names]|[Exact contiguous text copied from the source page]|[Reason why this chunk forms a distinct semantic unit and should remain separate from adjacent content]|[Exact text span from the source page]|


#### PAGE_CHUNK_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|[Source URL]|[ADD / DELETE / MERGE / SPLIT / MODIFY / REASSIGN]|[Short, precise description of the proposed chunking change]|[Reason why the change improves semantic coherence or retrieval quality]|[Exact text span supporting the change]|No|


#### PAGE_CHUNK_FINAL

|url|chunk_id|supported_intents|final_chunk|chunk_boundary_justification|evidence|
|-|-|-|-|-|-|
|[Source URL]|[chunk_name]|[Comma-separated approved intent names]|[Exact contiguous text copied from the source page]|[Reason why this approved chunk forms a distinct semantic unit and should remain separate from adjacent content]|[Exact text span from the source page]|


#### CHUNKING_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_CHUNK_CANDIDATES and PAGE_CHUNK_CHANGE_PROPOSALS conform to their expected schemas.|No|
|check_coverage|check_intent_chunk_coverage|Verify that every intent in PAGE_INTENT_FINAL is supported by one or more candidate chunks.|No|
|check_evidence|check_chunk_grounding|Verify that every candidate chunk and every proposed chunking change is supported by evidence from the source page.|No|
|check_boundaries|check_chunk_boundaries|Verify that chunk boundaries preserve coherent semantic units and do not unnecessarily split procedures or combine unrelated customer goals.|No|
|check_reasoning|check_chunk_change_reasons|Verify that every proposed ADD, DELETE, MERGE, SPLIT, MODIFY, or REASSIGN operation is reasonable and clearly justified.|No|
|check_retrieval|check_retrieval_quality|Verify that the proposed chunking supports effective semantic retrieval for the approved intents.|No|


#### USER_APPROVAL_CHUNK_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|[Source URL]|[ADD / DELETE / MERGE / SPLIT / MODIFY / REASSIGN]|[Short, precise description of the proposed chunking change]|[Reason why the change improves semantic coherence or retrieval quality]|[Exact text span supporting the change]|[APPROVED / REJECTED]|


## NOTES

notes.md records semantic observations that may assist future chunk generation,
retrieval optimization, and corpus-wide taxonomy consolidation.

Record information such as:

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
- accepted proposals
- rejected proposals
- audit history

These belong exclusively in curation.md.


