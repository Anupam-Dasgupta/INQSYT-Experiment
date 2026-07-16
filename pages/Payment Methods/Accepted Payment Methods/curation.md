### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|check_accepted_payment_methods|Check which credit, debit, or prepaid cards and payment networks are accepted on Amazon.com.|Amazon.com accepts a variety of payment options, including credit and debit cards. The following payment methods are available for use:|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|manage_payment_details|Add a new payment card or update existing payment details in Amazon Wallet.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_gift_card|Use an Amazon Gift Card to pay for an order.|You can also use Amazon Gift Cards to pay for your order.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|split_payment_with_gift_card|Pay for an order by splitting the payment between an accepted credit/debit card and an Amazon Gift Card.|You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_fsa_hsa|Use a Flexible Spending Account (FSA) or Health Savings Account (HSA) to purchase eligible items.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|pay_with_snap_ebt|Use a SNAP EBT card from a participating state as a payment method for eligible items.|SNAP EBT cards are accepted as payment methods for valid cards from participating states. For more information, visit www.amazon.com/SNAP. EBT Cash benefits are not available as a payment method.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|ADD|Add intent 'check_accepted_payment_methods'|Add a broad intent to cover viewing general accepted credit, debit, prepaid cards, and payment networks.|Amazon.com accepts a variety of payment options, including credit and debit cards. The following payment methods are available for use:|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|ADD|Add intent 'manage_payment_details'|Add an intent to cover adding a new card or updating existing card details in Amazon Wallet.|You can add a completely new payment card or change your existing payment details, without having to place an order, in your Amazon Wallet.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|ADD|Add intent 'pay_with_gift_card'|Add an intent to cover paying with Amazon Gift Cards, including payment splitting rules.|You can also use Amazon Gift Cards to pay for your order.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|MERGE|Merge candidate 'split_payment_with_gift_card' into 'pay_with_gift_card'|Splitting payment is a specific rule/condition of paying with Gift Cards and does not warrant a separate intent.|You can split payment between one of the accepted credit or debit cards and an Amazon.com Gift Card, but you can't split payment among multiple cards.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|ADD|Add intent 'pay_with_fsa_hsa'|Add an intent to cover paying with FSA or HSA benefits for eligible items.|We accept Flexible Spending Accounts (FSA), Health Savings Accounts (HSA) (U.S. billing addresses only) for the purchase of FSA or HSA eligible items.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GFBWMNXEPYVJAY9A|ADD|Add intent 'pay_with_snap_ebt'|Add an intent to cover using SNAP EBT cards from participating states as payment.|SNAP EBT cards are accepted as payment methods for valid cards from participating states.|No|

### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
