### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GACF9K9BWLFMF8ZN|check_currency_converter_supported_currencies|Check which currencies and card brands (Visa, MasterCard, or American Express) are supported by the Amazon Currency Converter, including estimated shipping windows.|Amazon Currency Converter is available when you use a Visa, MasterCard, or American Express credit or debit card denominated in a supported currency. The Amazon Currency Converter supports these currencies:|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GACF9K9BWLFMF8ZN|ADD|Add intent 'check_currency_converter_supported_currencies'|Add a broad intent to cover checking supported currencies, card brand eligibility, and shipping windows for the Amazon Currency Converter.|Amazon Currency Converter is available when you use a Visa, MasterCard, or American Express credit or debit card denominated in a supported currency. The Amazon Currency Converter supports these currencies:|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GACF9K9BWLFMF8ZN|ADD|Add intent 'check_currency_converter_supported_currencies'|Add a broad intent to cover checking supported currencies, card brand eligibility, and shipping windows for the Amazon Currency Converter.|Amazon Currency Converter is available when you use a Visa, MasterCard, or American Express credit or debit card denominated in a supported currency. The Amazon Currency Converter supports these currencies:|APPROVED|
