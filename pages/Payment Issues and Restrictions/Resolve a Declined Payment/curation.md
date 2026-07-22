### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G6P826S3WMEV8SPN|resolve_declined_payment|Resolve a declined payment on an order by troubleshooting common decline reasons, retrying with the current payment method, or selecting a different payment method.|To protect your security and privacy, your bank can't provide Amazon with information about why your payment was declined. ... To retry a declined payment, go to Your Orders.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G6P826S3WMEV8SPN|ADD|Add intent 'resolve_declined_payment'|Add a broad intent to cover troubleshooting, retrying, and changing payment methods for a declined order.|To retry a declined payment, go to Your Orders.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G6P826S3WMEV8SPN|ADD|Add intent 'resolve_declined_payment'|Add a broad intent to cover troubleshooting, retrying, and changing payment methods for a declined order.|To retry a declined payment, go to Your Orders.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G6P826S3WMEV8SPN|resolve_declined_payment||Resolve a declined payment on an order by troubleshooting common decline reasons, retrying with the current payment method, or selecting a different payment method.|To retry a declined payment, go to Your Orders.|
