### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|return_amazon_device|Learn rules, instructions, and procedures for returning Amazon devices and accessories.|What is your return policy for Amazon devices?... How do I return my Amazon device to Amazon.com? Prepare device for shipping... Print a mailing label... Give return package to the shipper...|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|check_device_warranty|Check limited warranty terms and request warranty service for Amazon devices and accessories.|Is my Amazon device or accessory covered by a limited warranty? Whether you bought your Amazon device through Amazon.com or in a retail store... new and Certified Refurbished devices are covered by a limited warranty.|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|deregister_amazon_device|Deregister an Amazon device from the Manage Your Content and Devices (MYCD) page.|Prior to returning it. Go to www.amazon.com/mycd. After logging in, go to the Devices tab. Select the device you are returning, and using the menu button, select "Deregister."|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|check_device_refund_policy|Check refund guidelines and shipping reimbursement rules for returned Amazon devices.|How will I be refunded for a returned device or accessory? All refunds are subject to our refunds policy... Pre-paid mailing labels and shipping cost refunds...|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|ADD|Add intent 'return_amazon_device'|Add a primary super-intent to return or manage Amazon devices.|What is your return policy for Amazon devices?... How do I return my Amazon device to Amazon.com? Prepare device for shipping... Print a mailing label... Give return package to the shipper...|No|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'check_device_warranty' into super-intent 'return_amazon_device'|Merge checking device and accessory limited warranty terms as a sub-intent.|Is my Amazon device or accessory covered by a limited warranty? Whether you bought your Amazon device through Amazon.com or in a retail store... new and Certified Refurbished devices are covered by a limited warranty.|No|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'deregister_amazon_device' into super-intent 'return_amazon_device'|Merge device deregistration prior to returns as a sub-intent.|Prior to returning it. Go to www.amazon.com/mycd. After logging in, go to the Devices tab. Select the device you are returning, and using the menu button, select "Deregister."|No|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'check_device_refund_policy' into super-intent 'return_amazon_device'|Merge checking device refund and shipping reimbursement rules as a sub-intent.|How will I be refunded for a returned device or accessory? All refunds are subject to our refunds policy... Pre-paid mailing labels and shipping cost refunds...|No|

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
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|ADD|Add intent 'return_amazon_device'|Add a primary super-intent to return or manage Amazon devices.|What is your return policy for Amazon devices?... How do I return my Amazon device to Amazon.com? Prepare device for shipping... Print a mailing label... Give return package to the shipper...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'check_device_warranty' into super-intent 'return_amazon_device'|Merge checking device and accessory limited warranty terms as a sub-intent.|Is my Amazon device or accessory covered by a limited warranty? Whether you bought your Amazon device through Amazon.com or in a retail store... new and Certified Refurbished devices are covered by a limited warranty.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'prepare_amazon_device_for_shipping' into super-intent 'return_amazon_device'|Merge steps for preparing a device for return shipment (package, deregistration, clearing data) as a sub-intent.|Prepare device for shipping: While Amazon will perform a factory reset... remove any data stored... Go to www.amazon.com/mycd... select Deregister.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|MERGE|Merge candidate 'check_device_refund_policy' into super-intent 'return_amazon_device'|Merge checking device refund and shipping reimbursement rules as a sub-intent.|How will I be refunded for a returned device or accessory? All refunds are subject to our refunds policy... Pre-paid mailing labels and shipping cost refunds...|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|return_amazon_device|check_device_warranty|Check limited warranty terms and request warranty service for Amazon devices and accessories.|Is my Amazon device or accessory covered by a limited warranty? Whether you bought your Amazon device through Amazon.com or in a retail store... new and Certified Refurbished devices are covered by a limited warranty.|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|return_amazon_device|prepare_amazon_device_for_shipping|Prepare an Amazon device for return shipment (packaging, deregistering via MYCD, factory reset).|Prepare device for shipping: While Amazon will perform a factory reset... remove any data stored... Go to www.amazon.com/mycd... select Deregister.|
|https://www.amazon.com/gp/help/customer/display.html/ref=help_hnf_p2_exp_201818950?nodeId=201818950|return_amazon_device|check_device_refund_policy|Check refund guidelines and shipping reimbursement rules for returned Amazon devices.|How will I be refunded for a returned device or accessory? All refunds are subject to our refunds policy... Pre-paid mailing labels and shipping cost refunds...|
