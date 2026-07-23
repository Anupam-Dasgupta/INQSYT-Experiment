### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|identify_fake_websites|Identify fake or spoofed websites pretending to be from Amazon by checking for IP-based addresses, URL spelling errors, mismatched hover links, and HTTPS security.|Scammers will try to get you to provide your information by providing you with websites that look like Amazon. Fake websites can be difficult to identify. Here are some red flags indicating that a website may be fake: Numerical addresses such as http://123.456.789... Misspellings or grammatical errors in the address... When hovering over a link, you notice a different address than what is displayed... Use secure addresses beginning with 'https://'.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|check_order_history|Review Amazon order history to verify if correspondence received regarding an unknown order is legitimate.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|report_suspicious_website|Report a suspicious website pretending to be from Amazon.|To report a suspicious website, visit Report a Scam.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|ADD|Add intent 'identify_fake_websites'|Add a primary intent for identifying fake or spoofed websites pretending to be from Amazon.|Numerical addresses such as http://123.456.789... Misspellings or grammatical errors in the address... When hovering over a link, you notice a different address than what is displayed... Use secure addresses beginning with 'https://'.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_websites'|Checking order history is a specific verification sub-step for identifying if a website is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|DELETE|Delete candidate 'report_suspicious_website'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|To report a suspicious website, visit Report a Scam.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|ADD|Add intent 'identify_fake_websites'|Add a primary intent for identifying fake or spoofed websites pretending to be from Amazon.|Numerical addresses such as http://123.456.789... Misspellings or grammatical errors in the address... When hovering over a link, you notice a different address than what is displayed... Use secure addresses beginning with 'https://'.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|MERGE|Merge candidate 'check_order_history' into super-intent 'identify_fake_websites'|Checking order history is a specific verification sub-step for identifying if a website is fake, rather than a standalone capability of this page.|If you received correspondence regarding an order you didn't place, it likely wasn't from Amazon. Visit Your Orders to review your order history.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|DELETE|Delete candidate 'report_suspicious_website'|Reporting scams is a distinct customer goal handled by the dedicated \"Report a scam\" page, and this page only provides links to it.|To report a suspicious website, visit Report a Scam.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=TFdMXlDPP3fvF122x1|identify_fake_websites||Identify fake or spoofed websites pretending to be from Amazon by checking for IP-based addresses, URL spelling errors, mismatched hover links, and HTTPS security.|Scammers will try to get you to provide your information by providing you with websites that look like Amazon. Fake websites can be difficult to identify. Here are some red flags indicating that a website may be fake: Numerical addresses such as http://123.456.789... Misspellings or grammatical errors in the address... When hovering over a link, you notice a different address than what is displayed... Use secure addresses beginning with 'https://'.|
