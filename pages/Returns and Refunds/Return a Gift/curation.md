### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|return_gift|Return a gift received from someone else using the order number.|The Returns Center allows gift recipients to return items marked as a gift at the time of purchase. To return a gift, go directly to Gift Returns.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|exchange_or_replace_gift|Exchange or replace a received gift.|If you received a gift and need an exchange or replacement, you'll need to return the gift and place a new order. If you’re the gift giver, you can request a replacement in Your Orders.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|find_gift_order_number|Find the 17-digit order number for a gift return.|To start a gift return you will need your order number. You can find your 17-digit order number on your packing slip that came with your item. You can also find it on the digital gift receipt we emailed you.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|request_gift_return|Request and process a gift return in the Returns Center.|Go to the Returns Center... Enter the order number... Select search... Select items... Select preferred return method... Follow instructions...|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|ADD|Add intent 'return_gift'|Add a primary super-intent to return or exchange items received as gifts.|The Returns Center allows gift recipients to return items marked as a gift at the time of purchase. To return a gift, go directly to Gift Returns.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'exchange_or_replace_gift' into super-intent 'return_gift'|Merge exchanging or replacing a gift as a specific sub-intent under return_gift.|If you received a gift and need an exchange or replacement, you'll need to return the gift and place a new order. If you’re the gift giver, you can request a replacement in Your Orders.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'find_gift_order_number' into super-intent 'return_gift'|Merge finding the gift's order number as a specific sub-intent under return_gift.|To start a gift return you will need your order number. You can find your 17-digit order number on your packing slip that came with your item. You can also find it on the digital gift receipt we emailed you.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'request_gift_return' into super-intent 'return_gift'|Merge steps for submitting a gift return request as a sub-intent under return_gift.|Go to the Returns Center... Enter the order number... Select search... Select items... Select preferred return method... Follow instructions...|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|ADD|Add intent 'return_gift'|Add a primary super-intent to return or exchange items received as gifts.|The Returns Center allows gift recipients to return items marked as a gift at the time of purchase. To return a gift, go directly to Gift Returns.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'exchange_or_replace_gift' into super-intent 'return_gift'|Merge exchanging or replacing a gift as a specific sub-intent under return_gift.|If you received a gift and need an exchange or replacement, you'll need to return the gift and place a new order. If you’re the gift giver, you can request a replacement in Your Orders.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'find_gift_order_number' into super-intent 'return_gift'|Merge finding the gift's order number as a specific sub-intent under return_gift.|To start a gift return you will need your order number. You can find your 17-digit order number on your packing slip that came with your item. You can also find it on the digital gift receipt we emailed you.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|MERGE|Merge candidate 'check_gift_return_considerations' into super-intent 'return_gift'|Merge checking rules, refund options, and things to consider before returning a gift.|Gift items valued at over $2,000 can only be refunded to the original payment method... Once we receive the returned item, we'll issue a refund to your Amazon.com Gift Card...|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|return_gift|exchange_or_replace_gift|Exchange or replace a received gift.|If you received a gift and need an exchange or replacement, you'll need to return the gift and place a new order. If you’re the gift giver, you can request a replacement in Your Orders.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|return_gift|find_gift_order_number|Find the 17-digit order number for a gift return.|To start a gift return you will need your order number. You can find your 17-digit order number on your packing slip that came with your item. You can also find it on the digital gift receipt we emailed you.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GMTDJ6XPUMN7NWNB|return_gift|check_gift_return_considerations|Check rules, limitations, and refund options to consider before returning a gift.|Gift items valued at over $2,000 can only be refunded to the original payment method of the purchaser... How We Process Your Refund: Once we receive the returned item, we'll issue a refund to your Amazon.com Gift Card balance...|
