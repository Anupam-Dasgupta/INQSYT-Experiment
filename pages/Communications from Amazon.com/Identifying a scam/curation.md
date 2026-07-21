### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|verify_amazon_communication|Verify whether a received call, email, text message, website, or other communication is from Amazon or an impersonation scam using verification tools.|If you've received a suspicious email, call, or message claiming to be from Amazon, verify it before taking action — forward it to verify@amazon.com or submit it by selecting the button below: Verify a call or message|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|report_amazon_scam|Report a suspicious email, phone call, text message, website, or other impersonation scam pretending to be from Amazon.|To report a suspicious message, click: Report a scam ... If you have received suspicious communication claiming to be from Amazon and you don't have an account with us, report it at reportascam@amazon.com.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|ADD|Add intent 'verify_amazon_communication'|Add an intent for checking the authenticity of emails, texts, calls, or websites pretending to be from Amazon using verification tools.|If you've received a suspicious email, call, or message claiming to be from Amazon, verify it before taking action — forward it to verify@amazon.com or submit it by selecting the button below: Verify a call or message|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|ADD|Add intent 'report_amazon_scam'|Add an intent for reporting fake emails, calls, texts, or websites pretending to be from Amazon.|To report a suspicious message, click: Report a scam ... If you have received suspicious communication claiming to be from Amazon and you don't have an account with us, report it at reportascam@amazon.com.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|ADD|Add intent 'verify_amazon_communication'|Add an intent for checking the authenticity of emails, texts, calls, or websites pretending to be from Amazon using verification tools.|If you've received a suspicious email, call, or message claiming to be from Amazon, verify it before taking action — forward it to verify@amazon.com or submit it by selecting the button below: Verify a call or message|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4YFYCCNUSENA23B|ADD|Add intent 'report_amazon_scam'|Add an intent for reporting fake emails, calls, texts, or websites pretending to be from Amazon.|To report a suspicious message, click: Report a scam ... If you have received suspicious communication claiming to be from Amazon and you don't have an account with us, report it at reportascam@amazon.com.|REJECTED|
