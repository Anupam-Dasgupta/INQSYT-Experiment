### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSNBBJP63SM65UDB|identify_unknown_charge|Identify or troubleshoot unknown or unrecognized Amazon charges on credit card or bank statements using transaction history and statement descriptors.|An unknown Amazon charge is probably an Amazon Prime payment, a digital service payment, an Amazon Pay transaction, or a bank authorization. ... For help identifying the unknown charge, refer to the list of commonly seen descriptors on bank/card statements:|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSNBBJP63SM65UDB|ADD|Add intent 'identify_unknown_charge'|Add a broad intent to cover identifying or troubleshooting unknown or unrecognized charges on bank or credit card statements.|For help identifying the unknown charge, refer to the list of commonly seen descriptors on bank/card statements:|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSNBBJP63SM65UDB|ADD|Add intent 'identify_unknown_charge'|Add a broad intent to cover identifying or troubleshooting unknown or unrecognized charges on bank or credit card statements.|For help identifying the unknown charge, refer to the list of commonly seen descriptors on bank/card statements:|APPROVED|
