### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|report_amazon_scam|Report a suspicious email, phone call, text message, website, or other impersonation scam pretending to be from Amazon.|If you receive a correspondence you think may not be from Amazon, report it immediately. To have the best advice on what actions to take, select the most appropriate link: ... If you don't have an Amazon account: You can still report suspicious communication to us at reportascam@amazon.com.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|report_scam_to_ftc|Report suspicious phone calls, text messages, or emails to the Federal Trade Commission (FTC).|To report suspicious phone calls or SMS/text messages to the Federal Trade Commission (FTC), visit https://reportfraud.ftc.gov and follow the onscreen assistant.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|ADD|Add intent 'report_amazon_scam'|Add the primary customer goal of reporting fake emails, calls, texts, or websites pretending to be from Amazon.|If you receive a correspondence you think may not be from Amazon, report it immediately. To have the best advice on what actions to take, select the most appropriate link: ... If you don't have an Amazon account: You can still report suspicious communication to us at reportascam@amazon.com.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|DELETE|Delete candidate intent 'report_scam_to_ftc'|Reporting to the FTC is a secondary external option. A separate intent is too granular and unnecessary since the primary action is reporting scams.|To report suspicious phone calls or SMS/text messages to the Federal Trade Commission (FTC), visit https://reportfraud.ftc.gov and follow the onscreen assistant.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|ADD|Add intent 'report_amazon_scam'|Add the primary customer goal of reporting fake emails, calls, texts, or websites pretending to be from Amazon.|If you receive a correspondence you think may not be from Amazon, report it immediately. To have the best advice on what actions to take, select the most appropriate link: ... If you don't have an Amazon account: You can still report suspicious communication to us at reportascam@amazon.com.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|DELETE|Delete candidate intent 'report_scam_to_ftc'|Reporting to the FTC is a secondary external option. A separate intent is too granular and unnecessary since the primary action is reporting scams.|To report suspicious phone calls or SMS/text messages to the Federal Trade Commission (FTC), visit https://reportfraud.ftc.gov and follow the onscreen assistant.|REJECTED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|report_amazon_scam||Report a suspicious email, phone call, text message, website, or other impersonation scam pretending to be from Amazon.|If you receive a correspondence you think may not be from Amazon, report it immediately. To have the best advice on what actions to take, select the most appropriate link: ... If you don't have an Amazon account: You can still report suspicious communication to us at reportascam@amazon.com.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GRGRY7AQ3LMPXVCV|report_scam_to_ftc||Report suspicious phone calls, text messages, or emails to the Federal Trade Commission (FTC).|To report suspicious phone calls or SMS/text messages to the Federal Trade Commission (FTC), visit https://reportfraud.ftc.gov and follow the onscreen assistant.|
