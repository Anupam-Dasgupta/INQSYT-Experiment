### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G3KGTPA8B42CKBJ4|avoid_payment_scams|Learn how to identify and avoid internet payment scams, phishing attempts, and fraudulent sellers pretending to represent Amazon.|Protect yourself from fraud on the internet by identifying and avoiding internet scams and phishing attempts. ... To avoid payment scams:|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G3KGTPA8B42CKBJ4|ADD|Add intent 'avoid_payment_scams'|Add a broad intent to cover safety guidelines, identifying fraudulent behavior, and avoiding payment scams.|To avoid payment scams:|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G3KGTPA8B42CKBJ4|ADD|Add intent 'avoid_payment_scams'|Add a broad intent to cover safety guidelines, identifying fraudulent behavior, and avoiding payment scams.|To avoid payment scams:|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G3KGTPA8B42CKBJ4|avoid_payment_scams||Learn how to identify and avoid internet payment scams, phishing attempts, and fraudulent sellers pretending to represent Amazon.|To avoid payment scams:|
