### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|Check which credit, debit, or prepaid cards and payment networks are accepted on Amazon.com.|Amazon.com accepts a variety of payment options, including credit and debit cards. The following payment methods are available for use:|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|manage_payment_details|Add a new payment card or change existing payment details in Amazon Wallet.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_gift_card|Pay for an order using an Amazon Gift Card, including rules for split payments.|You can also use Amazon Gift Cards to pay for your order. Note: You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_fsa_hsa|Use a Flexible Spending Account (FSA) or Health Savings Account (HSA) for U.S. billing addresses to purchase eligible items.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_snap_ebt|Use a SNAP EBT card from a participating state to purchase eligible items.|SNAP EBT cards are accepted as payment methods for valid cards from participating states. For more information, visit www.amazon.com/SNAP . EBT Cash benefits are not available as a payment method.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'manage_payment_details' into super-intent 'check_accepted_payment_methods'|Add 'manage_payment_details' as a sub-intent of 'check_accepted_payment_methods' to capture Wallet management rules.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_gift_card' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_gift_card' as a sub-intent of 'check_accepted_payment_methods' to capture gift card and split payment rules.|You can also use Amazon Gift Cards to pay for your order. Note: You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_fsa_hsa' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_fsa_hsa' as a sub-intent of 'check_accepted_payment_methods' to capture FSA/HSA card rules.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_snap_ebt' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_snap_ebt' as a sub-intent of 'check_accepted_payment_methods' to capture SNAP EBT card rules.|SNAP EBT cards are accepted as payment methods for valid cards from participating states. For more information, visit www.amazon.com/SNAP . EBT Cash benefits are not available as a payment method.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'manage_payment_details' into super-intent 'check_accepted_payment_methods'|Add 'manage_payment_details' as a sub-intent of 'check_accepted_payment_methods' to capture Wallet management rules.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_gift_card' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_gift_card' as a sub-intent of 'check_accepted_payment_methods' to capture gift card and split payment rules.|You can also use Amazon Gift Cards to pay for your order. Note: You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_fsa_hsa' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_fsa_hsa' as a sub-intent of 'check_accepted_payment_methods' to capture FSA/HSA card rules.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'pay_with_snap_ebt' into super-intent 'check_accepted_payment_methods'|Add 'pay_with_snap_ebt' as a sub-intent of 'check_accepted_payment_methods' to capture SNAP EBT card rules.|SNAP EBT cards are accepted as payment methods for valid cards from participating states. For more information, visit www.amazon.com/SNAP . EBT Cash benefits are not available as a payment method.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|manage_payment_details|Add a new payment card or change existing payment details in Amazon Wallet.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|pay_with_gift_card|Pay for an order using an Amazon Gift Card, including rules for split payments.|You can also use Amazon Gift Cards to pay for your order. Note: You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|pay_with_fsa_hsa|Use a Flexible Spending Account (FSA) or Health Savings Account (HSA) for U.S. billing addresses to purchase eligible items.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|pay_with_snap_ebt|Use a SNAP EBT card from a participating state to purchase eligible items.|SNAP EBT cards are accepted as payment methods for valid cards from participating states. For more information, visit www.amazon.com/SNAP . EBT Cash benefits are not available as a payment method.|
