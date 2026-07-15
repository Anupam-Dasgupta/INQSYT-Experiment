#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|check_currency_converter_exchange_rates|Check how exchange rates are used, updated, and determined when using the Amazon Currency Converter.|When Amazon Currency Converter is enabled, the exchange rate is used to convert the order subtotal to your local currency. The exchange rate displayed at checkout may not match the rates published online or in other financial databases. Those exchange rates are generally inter-bank rates that are for wholesale amounts and aren't available to retail consumers. Amazon consistently works to negotiate competitive foreign exchange rates with our bank service provider. The exchange rates used for Amazon Currency Converter are generally updated daily.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|check_refund_exchange_rate|Check the exchange rate applied when receiving a refund for an item purchased using the Amazon Currency Converter.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|check_kindle_ebook_exchange_rates|Check where to find the exchange rate for Kindle ebooks.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|check_bank_fees_for_currency_converter|Check if additional bank fees apply when using the Amazon Currency Converter.|Note: When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent `check_currency_converter_exchange_rates` to the taxonomy.|The page outlines how exchange rates are used to convert checkout totals and how they are updated.|When Amazon Currency Converter is enabled, the exchange rate is used to convert the order subtotal to your local currency. The exchange rate displayed at checkout may not match the rates published online or in other financial databases. Those exchange rates are generally inter-bank rates that are for wholesale amounts and aren't available to retail consumers. Amazon consistently works to negotiate competitive foreign exchange rates with our bank service provider. The exchange rates used for Amazon Currency Converter are generally updated daily.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent `check_refund_exchange_rate` to the taxonomy.|The page explicitly supports checking exchange rates applied to returns.|If you return an item, we use the same exchange rate to calculate your refund, including any fees.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent `check_kindle_ebook_exchange_rates` to the taxonomy.|The page outlines where customers can view the exchange rates for Kindle ebooks.|For Kindle ebooks, the applicable exchange rate displays on the detail page.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDVF7JHSLREZFKL4|ADD|Add intent `check_bank_fees_for_currency_converter` to the taxonomy.|The page warns customers about possible extra bank fees when using the converter.|Note: When using Amazon Currency Converter, your bank may still charge you a fee. Please contact your bank regarding these fees.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|

