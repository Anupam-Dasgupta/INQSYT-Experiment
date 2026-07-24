### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|check_delivery_guarantees|Learn rules, conditions, and terms for orders placed with guaranteed delivery dates.|We offer guaranteed delivery on certain delivery speeds and select products. When guaranteed delivery is available on an order, we'll state this on the checkout page, with the associated delivery date and cost.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|claim_late_delivery_refund|Request a refund of shipping fees if a guaranteed delivery is late or not attempted by the promised date.|If we provide a guaranteed delivery date and a delivery attempt isn't made by this date, we'll refund any shipping fees associated with that order.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|check_order_countdown_timer|Check how the "order within" countdown timer affects guaranteed delivery availability.|The "order within" countdown timer provides the window of time in which you must place the order to receive your delivery by the date shown.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|ADD|Add intent 'check_delivery_guarantees'|Add a primary super-intent to check delivery guarantees terms and conditions.|We offer guaranteed delivery on certain delivery speeds and select products. When guaranteed delivery is available on an order, we'll state this on the checkout page, with the associated delivery date and cost.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|MERGE|Merge candidate 'claim_late_delivery_refund' into super-intent 'check_delivery_guarantees'|Merge claiming shipping fee refunds for late delivery as a sub-intent.|If we provide a guaranteed delivery date and a delivery attempt isn't made by this date, we'll refund any shipping fees associated with that order.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|MERGE|Merge candidate 'check_order_countdown_timer' into super-intent 'check_delivery_guarantees'|Merge checking order countdown timer rules as a sub-intent.|The "order within" countdown timer provides the window of time in which you must place the order to receive your delivery by the date shown.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|ADD|Add intent 'check_delivery_guarantees'|Add a primary super-intent to check delivery guarantees terms and conditions.|We offer guaranteed delivery on certain delivery speeds and select products. When guaranteed delivery is available on an order, we'll state this on the checkout page, with the associated delivery date and cost.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|MERGE|Merge candidate 'claim_late_delivery_refund' into super-intent 'check_delivery_guarantees'|Merge claiming shipping fee refunds for late delivery as a sub-intent.|If we provide a guaranteed delivery date and a delivery attempt isn't made by this date, we'll refund any shipping fees associated with that order.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|MERGE|Merge candidate 'check_order_countdown_timer' into super-intent 'check_delivery_guarantees'|Merge checking order countdown timer rules as a sub-intent.|The "order within" countdown timer provides the window of time in which you must place the order to receive your delivery by the date shown.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|check_delivery_guarantees|claim_late_delivery_refund|Request a refund of shipping fees if a guaranteed delivery is late or not attempted by the promised date.|If we provide a guaranteed delivery date and a delivery attempt isn't made by this date, we'll refund any shipping fees associated with that order.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GCNQVPEFZLZZVLVY|check_delivery_guarantees|check_order_countdown_timer|Check how the "order within" countdown timer affects guaranteed delivery availability.|The "order within" countdown timer provides the window of time in which you must place the order to receive your delivery by the date shown.|
