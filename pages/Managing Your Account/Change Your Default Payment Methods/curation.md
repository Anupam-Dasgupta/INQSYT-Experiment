#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4MVXVJB8QKE7MLW|change_default_payment_method|Select or change the default payment method for purchases in your Amazon account.|Go to Your Wallet. If you already have a default payment method selected, it will be listed first. Select the payment method to set as the default. Select Edit. Select the box Set as default payment method. You may need to complete authentication to default your payment method. Select Save.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4MVXVJB8QKE7MLW|update_subscription_payment_method|Update the default payment method specifically for existing subscriptions.|If you have existing subscriptions, you may be prompted to update your account. Select Update.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4MVXVJB8QKE7MLW|MERGE|Merge candidate intents `change_default_payment_method` and `update_subscription_payment_method` under a new super-intent `change_default_payment_methods`.|These two candidate intents represent related actions for changing default payment settings (general settings and subscription settings) and are best organized under a single super-intent `change_default_payment_methods` to maintain a clean hierarchical taxonomy.|Select or change your default payment method in Your Wallet ... If you have existing subscriptions, you may be prompted to update your account. Select Update.|No|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G4MVXVJB8QKE7MLW|MERGE|Merge candidate intents `change_default_payment_method` and `update_subscription_payment_method` under a new super-intent `change_default_payment_methods`.|These two candidate intents represent related actions for changing default payment settings (general settings and subscription settings) and are best organized under a single super-intent `change_default_payment_methods` to maintain a clean hierarchical taxonomy.|Select or change your default payment method in Your Wallet ... If you have existing subscriptions, you may be prompted to update your account. Select Update.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
