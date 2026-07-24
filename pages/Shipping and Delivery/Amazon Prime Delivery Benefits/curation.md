### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_benefits|Check delivery speeds, pricing, and general shipping benefits included with Amazon Prime.|Your Amazon Prime membership includes a variety of delivery benefits, including several speed options if you need to expedite your delivery.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_eligibility|Check item, address, and quantity eligibility criteria for Prime shipping benefits.|Items and Addresses Eligibility... FREE Two-Day Delivery... FREE One-Day Delivery... FREE Same-Day Delivery... Amazon Day Delivery... FREE Release-Date Delivery... FREE Standard Shipping... Ineligible...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_rates|Check shipping fees and pricing for Prime delivery speeds in contiguous and non-contiguous US locations.|Delivery Speeds and Member Prices (Contiguous U.S.)... Addresses in Alaska, Hawaii, and Puerto Rico...|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|ADD|Add intent 'check_prime_delivery_benefits'|Add a primary super-intent to check Prime delivery benefits.|Your Amazon Prime membership includes a variety of delivery benefits, including several speed options if you need to expedite your delivery.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|MERGE|Merge candidate 'check_prime_delivery_eligibility' into super-intent 'check_prime_delivery_benefits'|Merge checking item and address eligibility for Prime shipping speeds as a sub-intent.|Items and Addresses Eligibility... FREE Two-Day Delivery... FREE One-Day Delivery... FREE Same-Day Delivery... Amazon Day Delivery... FREE Release-Date Delivery... FREE Standard Shipping... Ineligible...|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|MERGE|Merge candidate 'check_prime_delivery_rates' into super-intent 'check_prime_delivery_benefits'|Merge checking shipping rates and pricing for Prime members as a sub-intent.|Delivery Speeds and Member Prices (Contiguous U.S.)... Addresses in Alaska, Hawaii, and Puerto Rico...|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|ADD|Add intent 'check_prime_delivery_benefits'|Add a primary super-intent to check Prime delivery benefits.|Your Amazon Prime membership includes a variety of delivery benefits, including several speed options if you need to expedite your delivery.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|MERGE|Merge candidate 'check_prime_delivery_eligibility' into super-intent 'check_prime_delivery_benefits'|Merge checking item and address eligibility for Prime shipping speeds as a sub-intent.|Items and Addresses Eligibility... FREE Two-Day Delivery... FREE One-Day Delivery... FREE Same-Day Delivery... Amazon Day Delivery... FREE Release-Date Delivery... FREE Standard Shipping... Ineligible...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|MERGE|Merge candidate 'check_prime_delivery_rates' into super-intent 'check_prime_delivery_benefits'|Merge checking shipping rates and pricing for Prime members as a sub-intent.|Delivery Speeds and Member Prices (Contiguous U.S.)... Addresses in Alaska, Hawaii, and Puerto Rico...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|MERGE|Merge candidate 'check_prime_delivery_speed' into super-intent 'check_prime_delivery_benefits'|Merge checking available shipping speeds (Two-Day, One-Day, Same-Day, etc.) as a sub-intent.|Your Amazon Prime membership includes a variety of delivery benefits, including several speed options if you need to expedite your delivery.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_benefits|check_prime_delivery_eligibility|Check item, address, and quantity eligibility criteria for Prime shipping benefits.|Items and Addresses Eligibility... FREE Two-Day Delivery... FREE One-Day Delivery... FREE Same-Day Delivery... Amazon Day Delivery... FREE Release-Date Delivery... FREE Standard Shipping... Ineligible...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_benefits|check_prime_delivery_rates|Check shipping fees and pricing for Prime delivery speeds in contiguous and non-contiguous US locations.|Delivery Speeds and Member Prices (Contiguous U.S.)... Addresses in Alaska, Hawaii, and Puerto Rico...|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GRPQFCNVUDYCBG24|check_prime_delivery_benefits|check_prime_delivery_speed|Check available Prime shipping speed options (Two-Day, One-Day, Same-Day, Release-Date, Standard, Amazon Day).|Your Amazon Prime membership includes a variety of delivery benefits, including several speed options if you need to expedite your delivery.|
