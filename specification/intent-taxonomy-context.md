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

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|[Source URL]|[verb_object]|[One-sentence description of the customer goal]|[Exact text span from the source page]|


