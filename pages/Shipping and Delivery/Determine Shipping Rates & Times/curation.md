### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GPXSWFZ4PXRN96N3|check_shipping_rates_and_times|Check how to determine the shipping rates and estimated delivery times for items in the shopping cart.|To determine the applicable shipping rate and time for items in your Cart: 1. Select Proceed to checkout. 2. Select or add your shipping address. 3. Select a shipping speed... 4. Select a payment method... 5. The total shipping & handling cost as well as the estimated date of delivery, is listed under Order Summary.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GPXSWFZ4PXRN96N3|ADD|Add intent 'check_shipping_rates_and_times'|Add a primary super-intent to check shipping rates and times.|To determine the applicable shipping rate and time for items in your Cart: 1. Select Proceed to checkout. 2. Select or add your shipping address. 3. Select a shipping speed... 4. Select a payment method... 5. The total shipping & handling cost as well as the estimated date of delivery, is listed under Order Summary.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GPXSWFZ4PXRN96N3|ADD|Add intent 'check_shipping_rates_and_times'|Add a primary super-intent to check shipping rates and times.|To determine the applicable shipping rate and time for items in your Cart: 1. Select Proceed to checkout. 2. Select or add your shipping address. 3. Select a shipping speed... 4. Select a payment method... 5. The total shipping & handling cost as well as the estimated date of delivery, is listed under Order Summary.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GPXSWFZ4PXRN96N3|check_shipping_rates_and_times||Check how to determine the shipping rates and estimated delivery times for items in the shopping cart.|To determine the applicable shipping rate and time for items in your Cart: 1. Select Proceed to checkout. 2. Select or add your shipping address. 3. Select a shipping speed... 4. Select a payment method... 5. The total shipping & handling cost as well as the estimated date of delivery, is listed under Order Summary.|
