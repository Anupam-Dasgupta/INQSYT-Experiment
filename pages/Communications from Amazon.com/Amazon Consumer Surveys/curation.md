### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|take_consumer_survey|Participate in online surveys hosted by Amazon or third-party sites to provide feedback on experiences with Amazon products and services.|We occasionally invite you to take online surveys about your experience with our products. Typically, these surveys are hosted on third-party sites.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|receive_survey_reward|Receive an online gift card reward offered as appreciation for completing an Amazon.com consumer survey.|Sometimes, Amazon.com offers an online gift card as a sign of appreciation for completing the survey. Normally, we send the gift card to the same email address within two weeks.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|report_survey_scam|Report a suspicious email or phishing attempt that mimics an Amazon survey and asks for sensitive security information.|Amazon.com surveys never ask you to provide any sensitive security information, such as account information, passwords, or social security numbers. If you receive an Amazon.com email inviting you to take a survey that requests this sort of information, notify us immediately at reportascam@amazon.com.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'take_consumer_survey'|Add an intent for taking online consumer surveys to provide feedback on experiences with Amazon products and services.|We occasionally invite you to take online surveys about your experience with our products. Typically, these surveys are hosted on third-party sites.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'receive_survey_reward'|Add an intent for receiving online gift card rewards for completing Amazon consumer surveys.|Sometimes, Amazon.com offers an online gift card as a sign of appreciation for completing the survey. Normally, we send the gift card to the same email address within two weeks.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'report_survey_scam'|Add an intent for reporting suspicious survey emails that request sensitive information.|Amazon.com surveys never ask you to provide any sensitive security information, such as account information, passwords, or social security numbers. If you receive an Amazon.com email inviting you to take a survey that requests this sort of information, notify us immediately at reportascam@amazon.com.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'take_consumer_survey'|Add an intent for taking online consumer surveys to provide feedback on experiences with Amazon products and services.|We occasionally invite you to take online surveys about your experience with our products. Typically, these surveys are hosted on third-party sites.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'receive_survey_reward'|Add an intent for receiving online gift card rewards for completing Amazon consumer surveys.|Sometimes, Amazon.com offers an online gift card as a sign of appreciation for completing the survey. Normally, we send the gift card to the same email address within two weeks.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|ADD|Add intent 'report_survey_scam'|Add an intent for reporting suspicious survey emails that request sensitive information.|Amazon.com surveys never ask you to provide any sensitive security information, such as account information, passwords, or social security numbers. If you receive an Amazon.com email inviting you to take a survey that requests this sort of information, notify us immediately at reportascam@amazon.com.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|take_consumer_survey||Participate in online surveys hosted by Amazon or third-party sites to provide feedback on experiences with Amazon products and services.|We occasionally invite you to take online surveys about your experience with our products. Typically, these surveys are hosted on third-party sites.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G58ZQEGH2H25HAQR|report_survey_scam||Report suspicious emails posing as Amazon surveys that request sensitive security information (e.g. passwords, account info, social security numbers) to reportascam@amazon.com.|Amazon.com surveys never ask you to provide any sensitive security information, such as account information, passwords, or social security numbers. If you receive an Amazon.com email inviting you to take a survey that requests this sort of information, notify us immediately at reportascam@amazon.com.|
