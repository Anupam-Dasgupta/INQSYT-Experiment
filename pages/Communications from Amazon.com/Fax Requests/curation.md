### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQ6X9K9358LDSJRA|verify_order_via_fax|Fax requested documentation to Amazon's secure fax line to verify an order.|You can fax additional information to verify your order. ... Please send the requested documentation to our secure fax line at 206-266-1838.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQ6X9K9358LDSJRA|ADD|Add intent 'verify_order_via_fax'|Add a flat intent for verifying an order by faxing requested documents to Amazon's secure fax line.|You can fax additional information to verify your order. ... Please send the requested documentation to our secure fax line at 206-266-1838.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQ6X9K9358LDSJRA|ADD|Add intent 'verify_order_via_fax'|Add a flat intent for verifying an order by faxing requested documents to Amazon's secure fax line.|You can fax additional information to verify your order. ... Please send the requested documentation to our secure fax line at 206-266-1838.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQ6X9K9358LDSJRA|verify_order_via_fax||Fax requested documentation to Amazon's secure fax line to verify an order.|You can fax additional information to verify your order. ... Please send the requested documentation to our secure fax line at 206-266-1838.|
