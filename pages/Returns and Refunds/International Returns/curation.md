### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|return_international_item|Learn rules, procedures, and options for returning items internationally to Amazon.com.|You can return items fulfilled by Amazon within 30 days of receipt of delivery in Your Orders... International Return Methods: UPS drop off, DHL Express drop off, DHL Express pickup, Return label provided at your own expense...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|schedule_dhl_pickup|Schedule a DHL Express pickup to return an international package.|DHL Express Pickup details: Schedule via MyDHL+ or phone.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|request_international_postage_refund|Request or claim return shipping cost refunds for international returns sent at own expense.|Return label provided at your own expense (up to $25 automatically refunded, contact CS for more if it exceeds)... Refund of remaining postage for defective/damaged/incorrect items.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|ADD|Add intent 'return_international_item'|Add a primary super-intent to return items internationally to Amazon.com.|You can return items fulfilled by Amazon within 30 days of receipt of delivery in Your Orders... International Return Methods: UPS drop off, DHL Express drop off, DHL Express pickup, Return label provided at your own expense...|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|MERGE|Merge candidate 'schedule_dhl_pickup' into super-intent 'return_international_item'|Merge scheduling DHL pickup as a specific sub-intent under return_international_item.|DHL Express Pickup details: Schedule via MyDHL+ or phone.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|MERGE|Merge candidate 'request_international_postage_refund' into super-intent 'return_international_item'|Merge requesting postage refunds as a specific sub-intent under return_international_item.|Return label provided at your own expense (up to $25 automatically refunded, contact CS for more if it exceeds)... Refund of remaining postage for defective/damaged/incorrect items.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|ADD|Add intent 'return_international_item'|Add a primary super-intent to return items internationally to Amazon.com.|You can return items fulfilled by Amazon within 30 days of receipt of delivery in Your Orders... International Return Methods: UPS drop off, DHL Express drop off, DHL Express pickup, Return label provided at your own expense...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|MERGE|Merge candidate 'schedule_dhl_pickup' into super-intent 'return_international_item'|Merge scheduling DHL pickup as a specific sub-intent under return_international_item.|DHL Express Pickup details: Schedule via MyDHL+ or phone.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|MERGE|Merge candidate 'request_international_postage_refund' into super-intent 'return_international_item'|Merge requesting postage refunds as a specific sub-intent under return_international_item.|Return label provided at your own expense (up to $25 automatically refunded, contact CS for more if it exceeds)... Refund of remaining postage for defective/damaged/incorrect items.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|MERGE|Merge candidate 'check_international_return_methods' into super-intent 'return_international_item'|Merge checking international return shipping options/methods as a sub-intent.|International Return Methods: UPS drop off, DHL Express drop off, DHL Express pickup, Return label provided at your own expense...|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|return_international_item|schedule_dhl_pickup|Schedule a DHL Express pickup to return an international package.|DHL Express Pickup details: Schedule via MyDHL+ or phone.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|return_international_item|request_international_postage_refund|Request or claim return shipping cost refunds for international returns sent at own expense.|Return label provided at your own expense (up to $25 automatically refunded, contact CS for more if it exceeds)... Refund of remaining postage for defective/damaged/incorrect items.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GP8L6BMXBTJHKUJW|return_international_item|check_international_return_methods|Check international return shipping options and return drop-off/pickup methods.|International Return Methods: UPS drop off, DHL Express drop off, DHL Express pickup, Return label provided at your own expense...|
