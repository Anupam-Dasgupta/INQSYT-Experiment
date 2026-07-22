### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|verify_email_for_new_account|Verify ownership of an email address when creating a new Amazon account by using the verification link sent via email.|To verify your email address when creating a new account: 1. Select the link in the verification email. This email is sent automatically after you attempt to create the new account. 2. Follow the on-screen instructions.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|troubleshoot_missing_verification_email|Troubleshoot not receiving the verification email when creating a new account by checking the email address and spam/junk folder.|Note: If you don't receive our verification email, do the following: * Confirm that you entered your email address correctly. * Check if the email is in your spam or junk folder.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|ADD|Add intent 'verify_email_for_new_account'|Add the parent intent for verifying email ownership when creating a new Amazon account.|To verify your email address when creating a new account: 1. Select the link in the verification email. This email is sent automatically after you attempt to create the new account. 2. Follow the on-screen instructions.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|MERGE|Merge candidate 'troubleshoot_missing_verification_email' into super-intent 'verify_email_for_new_account'|Add 'troubleshoot_missing_verification_email' as a sub-intent of 'verify_email_for_new_account' to capture email delivery troubleshooting steps.|Note: If you don't receive our verification email, do the following: * Confirm that you entered your email address correctly. * Check if the email is in your spam or junk folder.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|ADD|Add intent 'verify_email_for_new_account'|Add the parent intent for verifying email ownership when creating a new Amazon account.|To verify your email address when creating a new account: 1. Select the link in the verification email. This email is sent automatically after you attempt to create the new account. 2. Follow the on-screen instructions.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|MERGE|Merge candidate 'troubleshoot_missing_verification_email' into super-intent 'verify_email_for_new_account'|Add 'troubleshoot_missing_verification_email' as a sub-intent of 'verify_email_for_new_account' to capture email delivery troubleshooting steps.|Note: If you don't receive our verification email, do the following: * Confirm that you entered your email address correctly. * Check if the email is in your spam or junk folder.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|verify_email_for_new_account||Verify ownership of an email address when creating a new Amazon account by using the verification link sent via email.|To verify your email address when creating a new account: 1. Select the link in the verification email. This email is sent automatically after you attempt to create the new account. 2. Follow the on-screen instructions.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GU3U2EU63RCFDAP2|verify_email_for_new_account|troubleshoot_missing_verification_email|Troubleshoot not receiving the verification email when creating a new account by checking the email address and spam/junk folder.|Note: If you don't receive our verification email, do the following: * Confirm that you entered your email address correctly. * Check if the email is in your spam or junk folder.|
