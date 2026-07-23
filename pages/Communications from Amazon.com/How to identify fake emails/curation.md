### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|identify_fake_emails|Identify fake or spoofed emails pretending to be from Amazon by checking the Message Center, sender address, spelling, links, and attachments.|To check whether an email is from Amazon: Check Message Center. Message Center will have all email communication sent by Amazon. If the email doesn't appear in Message Center, then it wasn't sent by Amazon... Look for misspellings or added/substituted characters in the sender address... Typos, grammatical errors, or links to websites that resemble Amazon, but aren’t Amazon... Legitimate Amazon emails may include links to secure Amazon pages instead of attachments.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|check_order_history|Review Amazon order history to verify if correspondence received regarding an unknown order is legitimate.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|report_suspicious_email|Report suspicious emails or scams pretending to be from Amazon.|To report a suspicious email, visit Report a Scam. ... To report a suspicious email, Report a Scam now.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|ADD|Add intent 'identify_fake_emails'|Add a primary intent for identifying fake or spoofed emails pretending to be from Amazon.|To check whether an email is from Amazon: Check Message Center. Message Center will have all email communication sent by Amazon. If the email doesn't appear in Message Center, then it wasn't sent by Amazon... Look for misspellings or added/substituted characters in the sender address... Typos, grammatical errors, or links to websites that resemble Amazon, but aren’t Amazon... Legitimate Amazon emails may include links to secure Amazon pages instead of attachments.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_emails'|Checking order history is a specific verification sub-step for identifying if an email is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|DELETE|Delete candidate 'report_suspicious_email'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a suspicious email, visit Report a Scam. ... To report a suspicious email, Report a Scam now.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|ADD|Add intent 'identify_fake_emails'|Add a primary intent for identifying fake or spoofed emails pretending to be from Amazon.|To check whether an email is from Amazon: Check Message Center. Message Center will have all email communication sent by Amazon. If the email doesn't appear in Message Center, then it wasn't sent by Amazon... Look for misspellings or added/substituted characters in the sender address... Typos, grammatical errors, or links to websites that resemble Amazon, but aren’t Amazon... Legitimate Amazon emails may include links to secure Amazon pages instead of attachments.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_emails'|Checking order history is a specific verification sub-step for identifying if an email is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|DELETE|Delete candidate 'report_suspicious_email'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a suspicious email, visit Report a Scam. ... To report a suspicious email, Report a Scam now.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=Teu845SZK0ApsIgmGC|identify_fake_emails||Identify fake or spoofed emails pretending to be from Amazon by checking the Message Center, sender address, spelling, links, and attachments.|To check whether an email is from Amazon: Check Message Center. Message Center will have all email communication sent by Amazon. If the email doesn't appear in Message Center, then it wasn't sent by Amazon... Look for misspellings or added/substituted characters in the sender address... Typos, grammatical errors, or links to websites that resemble Amazon, but aren’t Amazon... Legitimate Amazon emails may include links to secure Amazon pages instead of attachments.|
