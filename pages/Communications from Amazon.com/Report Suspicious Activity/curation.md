### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_suspicious_product_or_seller|Report a suspicious, illegal, or unsafe product, or an issue with a seller, either directly on the product page or by contacting Customer Service.|Log into your Amazon account... Navigate to the product page, Select 'Report an issue with this product or seller', and Select 'This product or content is illegal, unsafe or suspicious' or 'I have an issue with a Seller' to report suspicious activity... If you would like to report a suspicious product or seller... speak with a Customer Service agent via phone or chat.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_stolen_property|Report suspected stolen goods being sold on Amazon to Customer Service, local law enforcement, or the California Office of the Attorney General.|If you suspect that a product for sale on Amazon.com is stolen, contact Customer Service. Use one of the methods on this page and immediately file a report with your local law enforcement agency. For California residents, report suspected stolen goods to the California Office of the Attorney General...|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_amazon_scam|Report a suspicious phone call, email, SMS message, unsolicited package, or gift card scam.|Follow the instructions in Report a Scam to report suspicious emails, phone calls, text messages, unsolicited packages, or gift card scams.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|ADD|Add intent 'report_suspicious_product_or_seller'|Add a primary intent for reporting suspicious products or sellers.|Log into your Amazon account... Navigate to the product page, Select 'Report an issue with this product or seller', and Select 'This product or content is illegal, unsafe or suspicious' or 'I have an issue with a Seller' to report suspicious activity... If you would like to report a suspicious product or seller... speak with a Customer Service agent via phone or chat.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|ADD|Add intent 'report_stolen_property'|Add a primary intent for reporting suspected stolen property listed on Amazon.|If you suspect that a product for sale on Amazon.com is stolen, contact Customer Service. Use one of the methods on this page and immediately file a report with your local law enforcement agency. For California residents, report suspected stolen goods to the California Office of the Attorney General...|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|DELETE|Delete candidate 'report_amazon_scam'|Reporting scams is a distinct customer goal handled by the dedicated "Report a scam" page, and this page only provides links to it.|Follow the instructions in Report a Scam to report suspicious emails, phone calls, text messages, unsolicited packages, or gift card scams.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|ADD|Add intent 'report_suspicious_activity'|Add a primary super-intent for general reporting of suspicious activities on Amazon.|Log into your Amazon account... Navigate to the product page... Select 'Report an issue with this product or seller'... contact Customer Service... immediately file a report...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|MERGE|Merge candidate 'report_suspicious_product_or_seller' into super-intent 'report_suspicious_activity'|Merge as a sub-intent of report_suspicious_activity to capture product/seller reporting.|Log into your Amazon account... Navigate to the product page, Select 'Report an issue with this product or seller', and Select 'This product or content is illegal, unsafe or suspicious' or 'I have an issue with a Seller' to report suspicious activity... If you would like to report a suspicious product or seller... speak with a Customer Service agent via phone or chat.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|MERGE|Merge candidate 'report_stolen_property' into super-intent 'report_suspicious_activity'|Merge as a sub-intent of report_suspicious_activity to capture stolen goods reporting.|If you suspect that a product for sale on Amazon.com is stolen, contact Customer Service. Use one of the methods on this page and immediately file a report with your local law enforcement agency. For California residents, report suspected stolen goods to the California Office of the Attorney General...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|MERGE|Merge candidate 'report_scam_call_message' into super-intent 'report_suspicious_activity'|Merge as a sub-intent of report_suspicious_activity to capture scam reporting (renamed from report_amazon_scam).|Follow the instructions in Report a Scam to report suspicious emails, phone calls, text messages, unsolicited packages, or gift card scams.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_suspicious_activity|report_suspicious_product_or_seller|Report a suspicious, illegal, or unsafe product, or an issue with a seller, either directly on the product page or by contacting Customer Service.|Log into your Amazon account... Navigate to the product page, Select 'Report an issue with this product or seller', and Select 'This product or content is illegal, unsafe or suspicious' or 'I have an issue with a Seller' to report suspicious activity... If you would like to report a suspicious product or seller... speak with a Customer Service agent via phone or chat.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_suspicious_activity|report_stolen_property|Report suspected stolen goods being sold on Amazon to Customer Service, local law enforcement, or the California Office of the Attorney General.|If you suspect that a product for sale on Amazon.com is stolen, contact Customer Service. Use one of the methods on this page and immediately file a report with your local law enforcement agency. For California residents, report suspected stolen goods to the California Office of the Attorney General...|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=T3MYikBay7swNeFqFo|report_suspicious_activity|report_scam_call_message|Report suspicious phone calls, text messages, emails, unsolicited packages, or gift card scams pretending to be from Amazon.|Follow the instructions in Report a Scam to report suspicious emails, phone calls, text messages, unsolicited packages, or gift card scams.|
