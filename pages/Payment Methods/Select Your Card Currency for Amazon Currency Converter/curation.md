### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GC6KVCQQQFWKPCGQ|select_card_currency_for_currency_converter|Select or change the card currency for the Amazon Currency Converter at checkout on desktop or mobile.|If your order is eligible for Amazon Currency Converter, the option to pay in your card currency will be displayed at checkout. ... If you want to change your card currency, you can update it at the checkout:|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GC6KVCQQQFWKPCGQ|ADD|Add intent 'select_card_currency_for_currency_converter'|Add a broad intent to cover selecting or changing card currency at checkout on desktop or mobile for the Amazon Currency Converter.|If your order is eligible for Amazon Currency Converter, the option to pay in your card currency will be displayed at checkout. ... If you want to change your card currency, you can update it at the checkout:|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GC6KVCQQQFWKPCGQ|ADD|Add intent 'select_card_currency_for_currency_converter'|Add a broad intent to cover selecting or changing card currency at checkout on desktop or mobile for the Amazon Currency Converter.|If your order is eligible for Amazon Currency Converter, the option to pay in your card currency will be displayed at checkout. ... If you want to change your card currency, you can update it at the checkout:|APPROVED|
