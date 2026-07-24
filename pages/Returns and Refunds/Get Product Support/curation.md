### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|get_product_support|Access help options (setup, troubleshooting, replacement parts, warranty repairs) for purchased items.|Need help with your product? Go to Get Product Support... We assist with issues such as product setup, troubleshooting, obtaining replacement parts, and facilitating warranty repairs.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|get_refund_or_replacement_fallback|Claim refund or replacement via Your Orders if product support is not available for an item.|If product support is not available for your item, go to Your Orders to get a refund or a replacement for a damaged, defective, or broken item.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|request_product_support|Learn how to request and use product support for an eligible item.|To get Product Support on your item: 1. Go to Product Support. 2. Select the product... 3. Select the support option...|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|ADD|Add intent 'get_product_support'|Add a primary super-intent to access product support options.|Need help with your product? Go to Get Product Support... We assist with issues such as product setup, troubleshooting, obtaining replacement parts, and facilitating warranty repairs.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|MERGE|Merge candidate 'get_refund_or_replacement_fallback' into super-intent 'get_product_support'|Merge getting refund/replacement fallback when product support is unavailable.|If product support is not available for your item, go to Your Orders to get a refund or a replacement for a damaged, defective, or broken item.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|MERGE|Merge candidate 'request_product_support' into super-intent 'get_product_support'|Merge steps to request product support on an item.|To get Product Support on your item: 1. Go to Product Support. 2. Select the product... 3. Select the support option...|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|ADD|Add intent 'get_product_support'|Add a primary super-intent to access product support options.|Need help with your product? Go to Get Product Support... We assist with issues such as product setup, troubleshooting, obtaining replacement parts, and facilitating warranty repairs.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|MERGE|Merge candidate 'get_refund_or_replacement_fallback' into super-intent 'get_product_support'|Merge getting refund/replacement fallback when product support is unavailable.|If product support is not available for your item, go to Your Orders to get a refund or a replacement for a damaged, defective, or broken item.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|MERGE|Merge candidate 'request_product_support' into super-intent 'get_product_support'|Merge steps to request product support on an item.|To get Product Support on your item: 1. Go to Product Support. 2. Select the product... 3. Select the support option...|REJECTED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=G94W2A3Y2Y6EQQPG|get_product_support||Access help options (setup, troubleshooting, replacement parts, warranty repairs) for purchased items.|Need help with your product? Go to Get Product Support... We assist with issues such as product setup, troubleshooting, obtaining replacement parts, and facilitating warranty repairs.|
