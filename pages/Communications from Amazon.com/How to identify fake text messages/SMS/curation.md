### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|identify_fake_sms|Identify fake or spoofed text messages (SMS) pretending to be from Amazon by checking the sender number, expected deliveries, and link addresses.|Scammers may send text messages claiming to be Amazon. These aren't from Amazon if they include: Phone numbers that you don't recognize or messages from a number with a country code... Text messages for orders or deliveries that you're not expecting... Text messages that contain phishing links with URLs that are misspelled, have typos, or have a link that is an IP address.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|check_order_history|Review Amazon order history to verify if a text message received regarding an unknown order is legitimate.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|report_suspicious_sms|Report a suspicious text message or scam pretending to be from Amazon.|To report a suspicious message, use the Report a Scam button|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|ADD|Add intent 'identify_fake_sms'|Add a primary intent for identifying fake or spoofed text messages (SMS) pretending to be from Amazon.|Scammers may send text messages claiming to be Amazon. These aren't from Amazon if they include: Phone numbers that you don't recognize or messages from a number with a country code... Text messages for orders or deliveries that you're not expecting... Text messages that contain phishing links with URLs that are misspelled, have typos, or have a link that is an IP address.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_sms'|Checking order history is a specific verification sub-step for identifying if an SMS is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|DELETE|Delete candidate 'report_suspicious_sms'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a suspicious message, use the Report a Scam button|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|ADD|Add intent 'identify_fake_sms'|Add a primary intent for identifying fake or spoofed text messages (SMS) pretending to be from Amazon.|Scammers may send text messages claiming to be Amazon. These aren't from Amazon if they include: Phone numbers that you don't recognize or messages from a number with a country code... Text messages for orders or deliveries that you're not expecting... Text messages that contain phishing links with URLs that are misspelled, have typos, or have a link that is an IP address.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_sms'|Checking order history is a specific verification sub-step for identifying if an SMS is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|DELETE|Delete candidate 'report_suspicious_sms'|Reporting scams is a distinct customer goal handled by the dedicated \"Report a scam\" page, and this page only provides links to it.|To report a suspicious message, use the Report a Scam button|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T2W6VB0DExBF3oyVvx|identify_fake_sms||Identify fake or spoofed text messages (SMS) pretending to be from Amazon by checking the sender number, expected deliveries, and link addresses.|Scammers may send text messages claiming to be Amazon. These aren't from Amazon if they include: Phone numbers that you don't recognize or messages from a number with a country code... Text messages for orders or deliveries that you're not expecting... Text messages that contain phishing links with URLs that are misspelled, have typos, or have a link that is an IP address.|
