### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|check_currency_converter_requirements|Check the qualification and order requirements to use the Amazon Currency Converter.|To qualify to use Amazon Currency Converter:|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|resolve_declined_currency_converter_payment|Resolve a declined payment on an Amazon Currency Converter order while maintaining the converter.|To resolve a declined payment on an Amazon Currency Converter order, you must use an eligible payment method denominated in the same currency as the original purchase to maintain Amazon Currency Converter.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|ADD|Add intent 'check_currency_converter_requirements'|Add a broad intent to cover qualification rules, eligible payment instruments, and order restrictions for the Amazon Currency Converter.|Use of Amazon Currency Converter is subject to certain requirements. To qualify to use Amazon Currency Converter:|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|MERGE|Merge candidate 'resolve_declined_currency_converter_payment' into 'check_currency_converter_requirements'|Resolving a declined payment is a specific condition and exception path for currency converter orders, better represented under the broader requirements intent.|To resolve a declined payment on an Amazon Currency Converter order, you must use an eligible payment method denominated in the same currency as the original purchase to maintain Amazon Currency Converter.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|ADD|Add intent 'check_currency_converter_requirements'|Add a broad intent to cover qualification rules, eligible payment instruments, and order restrictions for the Amazon Currency Converter.|Use of Amazon Currency Converter is subject to certain requirements. To qualify to use Amazon Currency Converter:|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|MERGE|Merge candidate 'resolve_declined_currency_converter_payment' into 'check_currency_converter_requirements'|Resolving a declined payment is a specific condition and exception path for currency converter orders, better represented under the broader requirements intent.|To resolve a declined payment on an Amazon Currency Converter order, you must use an eligible payment method denominated in the same currency as the original purchase to maintain Amazon Currency Converter.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|check_currency_converter_requirements||Check the qualification and order requirements to use the Amazon Currency Converter.|To qualify to use Amazon Currency Converter:|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GEC47LAK95ESY2JW|check_currency_converter_requirements|resolve_declined_currency_converter_payment|Resolve a declined payment on an Amazon Currency Converter order while maintaining the converter.|To resolve a declined payment on an Amazon Currency Converter order, you must use an eligible payment method denominated in the same currency as the original purchase to maintain Amazon Currency Converter.|
