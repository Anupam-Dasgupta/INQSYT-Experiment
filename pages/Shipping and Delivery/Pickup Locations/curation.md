### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|check_pickup_locations|Learn rules, carrier options, and procedures for delivering packages to pickup locations instead of home or business addresses.|Instead of having a package delivered to your home or business address, you can select a pickup point. You can choose to deliver eligible packages to pickup locations such as Amazon Locker, Amazon Counter, or UPS AccessPoints™ Locations.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|search_pickup_locations|Search and locate available pickup points near your area.|To find a pickup point near you, go to Amazon pickup.|

### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|ADD|Add intent 'check_pickup_locations'|Add a primary super-intent to return or manage Amazon devices.|Instead of having a package delivered to your home or business address, you can select a pickup point. You can choose to deliver eligible packages to pickup locations such as Amazon Locker, Amazon Counter, or UPS AccessPoints™ Locations.|No|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|MERGE|Merge candidate 'search_pickup_locations' into super-intent 'check_pickup_locations'|Merge searching and locating pickup points as a sub-intent under check_pickup_locations.|To find a pickup point near you, go to Amazon pickup.|No|

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
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|ADD|Add intent 'select_pickup_location'|Add a primary super-intent to select a pickup location.|Instead of having a package delivered to your home or business address, you can select a pickup point.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|MERGE|Merge candidate 'search_pickup_locations' into super-intent 'select_pickup_location'|Merge searching and locating pickup points as a sub-intent.|To find a pickup point near you, go to Amazon pickup.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|MERGE|Merge candidate 'check_opening_hours' into super-intent 'select_pickup_location'|Merge checking opening hours/operation times for pickup locations as a sub-intent.|Anticipated sub-intent for pickup location operating hours requested by user.|APPROVED|

### FINAL_INTENT_TABLE

|url|intent_name|sub-intent|intent_description|evidence|
|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GZTXM2L3YLZFSQ6W|select_pickup_location|check_opening_hours|Check opening hours, operation times, and accessibility schedules for a selected Amazon pickup location.|Anticipated sub-intent for pickup location operating hours requested by user.|
