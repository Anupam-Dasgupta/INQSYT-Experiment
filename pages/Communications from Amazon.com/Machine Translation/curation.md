### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU64X99NVH4MZBZW|use_machine_translation_for_chat|Contact Amazon customer service via chat in a preferred language using translation technology to communicate with agents who speak a different language.|This won't change anything for you and you can contact us in your language as usual. Translation technology shows the employee your request in their language, and you'll be answered in your language. Currently, this technology is only used for requests via chat.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU64X99NVH4MZBZW|ADD|Add intent 'use_machine_translation_for_chat'|Add an intent for communicating with customer service via chat in a preferred language using translation technology.|This won't change anything for you and you can contact us in your language as usual. Translation technology shows the employee your request in their language, and you'll be answered in your language. Currently, this technology is only used for requests via chat.|No|

### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|

### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU64X99NVH4MZBZW|ADD|Add intent 'use_machine_translation_for_chat'|Add an intent for communicating with customer service via chat in a preferred language using translation technology.|This won't change anything for you and you can contact us in your language as usual. Translation technology shows the employee your request in their language, and you'll be answered in your language. Currently, this technology is only used for requests via chat.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU64X99NVH4MZBZW|use_machine_translation_for_chat||Contact Amazon customer service via chat in a preferred language using translation technology to communicate with agents who speak a different language.|This won't change anything for you and you can contact us in your language as usual. Translation technology shows the employee your request in their language, and you'll be answered in your language. Currently, this technology is only used for requests via chat.|
