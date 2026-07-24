### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|check_refund_status|Check the status, details, and issuing progress of an Amazon return refund.|You can check your refund status in Your Returns... Go to Your Returns... Find the returned item in the Last 3 Months section. You'll be able to access your refund details.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|check_gift_refund_status|Verify the refund status, recipient, and payment destination for returned gifts.|Once we've processed a gift return, we'll issue a refund to the person who returned the gift... Gift recipient returns: The refund goes to the gift card balance... Gift purchaser returns: The refund goes to the refund method...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|check_refund_payment_details|View issued refund details, transaction summaries, and payment destinations.|Refunds go to the refund method that you select in the Online Returns Center... You'll find all refunds and transactions in Your Transactions.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|ADD|Add intent 'check_refund_status'|Add a primary super-intent to check status and progress of return refunds.|You can check your refund status in Your Returns... Go to Your Returns... Find the returned item in the Last 3 Months section. You'll be able to access your refund details.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|MERGE|Merge candidate 'check_gift_refund_status' into super-intent 'check_refund_status'|Merge gift refund checks as a specific sub-intent under check_refund_status.|Once we've processed a gift return, we'll issue a refund to the person who returned the gift... Gift recipient returns: The refund goes to the gift card balance... Gift purchaser returns: The refund goes to the refund method...|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|MERGE|Merge candidate 'check_refund_payment_details' into super-intent 'check_refund_status'|Merge checking issued refund details and transactions as a specific sub-intent under check_refund_status.|Refunds go to the refund method that you select in the Online Returns Center... You'll find all refunds and transactions in Your Transactions.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|ADD|Add intent 'check_refund_status'|Add a primary super-intent to check status and progress of return refunds.|You can check your refund status in Your Returns... Go to Your Returns... Find the returned item in the Last 3 Months section. You'll be able to access your refund details.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|MERGE|Merge candidate 'check_gift_refund_status' into super-intent 'check_refund_status'|Merge gift refund checks as a specific sub-intent under check_refund_status.|Once we've processed a gift return, we'll issue a refund to the person who returned the gift... Gift recipient returns: The refund goes to the gift card balance... Gift purchaser returns: The refund goes to the refund method...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|MERGE|Merge candidate 'check_refund_payment_details' into super-intent 'check_refund_status'|Merge checking issued refund details and transactions as a specific sub-intent under check_refund_status.|Refunds go to the refund method that you select in the Online Returns Center... You'll find all refunds and transactions in Your Transactions.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|check_refund_status|check_gift_refund_status|Verify the refund status, recipient, and payment destination for returned gifts.|Once we've processed a gift return, we'll issue a refund to the person who returned the gift... Gift recipient returns: The refund goes to the gift card balance... Gift purchaser returns: The refund goes to the refund method...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMP8PC8KBY5FCPM2|check_refund_status|check_refund_payment_details|View issued refund details, transaction summaries, and payment destinations.|Refunds go to the refund method that you select in the Online Returns Center... You'll find all refunds and transactions in Your Transactions.|
