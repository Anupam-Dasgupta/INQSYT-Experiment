### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_currency_converter_exchange_rates|Check how foreign exchange rates are calculated, updated, and applied to convert subtotals for the Amazon Currency Converter.|When Amazon Currency Converter is enabled, the exchange rate is used to convert the order subtotal to your local currency. The exchange rate displayed at checkout may not match the rates published online or in other financial databases... The exchange rates used for Amazon Currency Converter are generally updated daily.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_refund_exchange_rate|Check the exchange rate used to calculate refunds for returned items purchased using the Amazon Currency Converter.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|inquire_bank_currency_fees|Contact the card-issuing bank to understand any additional transaction or foreign exchange fees charged when using Amazon Currency Converter.|When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_kindle_ebook_exchange_rate|Check the applicable exchange rate for Kindle ebooks on the product detail page.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent 'check_currency_converter_exchange_rates'|Add a broad intent to cover checking the Currency Converter exchange rate calculation and updates.|When Amazon Currency Converter is enabled, the exchange rate is used to convert the order subtotal to your local currency. The exchange rate displayed at checkout may not match the rates published online or in other financial databases... The exchange rates used for Amazon Currency Converter are generally updated daily.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'check_refund_exchange_rate' into super-intent 'check_currency_converter_exchange_rates'|Add 'check_refund_exchange_rate' as a sub-intent of 'check_currency_converter_exchange_rates' to capture refund rate rules.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'inquire_bank_currency_fees' into super-intent 'check_currency_converter_exchange_rates'|Add 'inquire_bank_currency_fees' as a sub-intent of 'check_currency_converter_exchange_rates' to capture bank fee details.|When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'check_kindle_ebook_exchange_rate' into super-intent 'check_currency_converter_exchange_rates'|Add 'check_kindle_ebook_exchange_rate' as a sub-intent of 'check_currency_converter_exchange_rates' to capture Kindle ebook rates.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent 'check_currency_converter_exchange_rates'|Add a broad intent to cover checking the Currency Converter exchange rate calculation and updates.|When Amazon Currency Converter is enabled, the exchange rate is used to convert the order subtotal to your local currency. The exchange rate displayed at checkout may not match the rates published online or in other financial databases... The exchange rates used for Amazon Currency Converter are generally updated daily.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'check_refund_exchange_rate' into super-intent 'check_currency_converter_exchange_rates'|Add 'check_refund_exchange_rate' as a sub-intent of 'check_currency_converter_exchange_rates' to capture refund rate rules.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'inquire_bank_currency_fees' into super-intent 'check_currency_converter_exchange_rates'|Add 'inquire_bank_currency_fees' as a sub-intent of 'check_currency_converter_exchange_rates' to capture bank fee details.|When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|MERGE|Merge candidate 'check_kindle_ebook_exchange_rate' into super-intent 'check_currency_converter_exchange_rates'|Add 'check_kindle_ebook_exchange_rate' as a sub-intent of 'check_currency_converter_exchange_rates' to capture Kindle ebook rates.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_currency_converter_exchange_rates|check_refund_exchange_rate|Check the exchange rate used to calculate refunds for returned items purchased using the Amazon Currency Converter.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_currency_converter_exchange_rates|inquire_bank_currency_fees|Contact the card-issuing bank to understand any additional transaction or foreign exchange fees charged when using Amazon Currency Converter.|When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GDVF7JHSLREZFKL4|check_currency_converter_exchange_rates|check_kindle_ebook_exchange_rate|Check the applicable exchange rate for Kindle ebooks on the product detail page.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|
