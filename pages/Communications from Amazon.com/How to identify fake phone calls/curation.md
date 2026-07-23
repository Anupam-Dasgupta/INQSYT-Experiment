### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|identify_fake_phone_calls|Identify fake or spoofed phone calls pretending to be from Amazon by inspecting caller requests for payment, remote access, confidential details, or urgent actions.|If you receive a suspicious phone call from someone claiming to be from Amazon, be alert if they: Ask you for payment over the phone... Try to remotely access your device... Ask for your Amazon password, personal sensitive information... Create false emergencies by claiming your Amazon subscription is expiring or unauthorized purchases were made...|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|check_order_history|Review Amazon order history to verify if a phone call received regarding an unknown order is legitimate.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|report_suspicious_call|Report a suspicious phone call or scam pretending to be from Amazon.|To report a fake phone call, go to Report a Scam|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|ADD|Add intent 'identify_fake_phone_calls'|Add a primary intent for identifying fake or spoofed phone calls pretending to be from Amazon.|If you receive a suspicious phone call from someone claiming to be from Amazon, be alert if they: Ask you for payment over the phone... Try to remotely access your device... Ask for your Amazon password, personal sensitive information... Create false emergencies by claiming your Amazon subscription is expiring or unauthorized purchases were made...|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_phone_calls'|Checking order history is a specific verification sub-step for identifying if a phone call is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|DELETE|Delete candidate 'report_suspicious_call'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a fake phone call, go to Report a Scam|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|ADD|Add intent 'identify_fake_phone_calls'|Add a primary intent for identifying fake or spoofed phone calls pretending to be from Amazon.|If you receive a suspicious phone call from someone claiming to be from Amazon, be alert if they: Ask you for payment over the phone... Try to remotely access your device... Ask for your Amazon password, personal sensitive information... Create false emergencies by claiming your Amazon subscription is expiring or unauthorized purchases were made...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_phone_calls'|Checking order history is a specific verification sub-step for identifying if a phone call is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|DELETE|Delete candidate 'report_suspicious_call'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a fake phone call, go to Report a Scam|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3rnIphp327SSKYl8e|identify_fake_phone_calls||Identify fake or spoofed phone calls pretending to be from Amazon by inspecting caller requests for payment, remote access, confidential details, or urgent actions.|If you receive a suspicious phone call from someone claiming to be from Amazon, be alert if they: Ask you for payment over the phone... Try to remotely access your device... Ask for your Amazon password, personal sensitive information... Create false emergencies by claiming your Amazon subscription is expiring or unauthorized purchases were made...|
