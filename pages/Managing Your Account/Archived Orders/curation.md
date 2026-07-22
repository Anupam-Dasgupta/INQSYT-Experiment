#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=G7882F7JTSV9N5BS|view_archived_orders|View previously archived orders on the account.|You can view previously archived orders in Your Orders. To view previously archived orders: 1. Go to Your Orders. 2. Search for the relevant order, or filter for the date range that the order was originally purchased.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G7882F7JTSV9N5BS|ADD|Add intent `view_archived_orders` to the taxonomy.|The page provides direct instructions for how users can view previously archived orders in their Amazon account.|You can view previously archived orders in Your Orders. To view previously archived orders: 1. Go to Your Orders. 2. Search for the relevant order, or filter for the date range that the order was originally purchased.|No|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G7882F7JTSV9N5BS|ADD|Add intent `view_archived_orders` to the taxonomy.|The page provides direct instructions for how users can view previously archived orders in their Amazon account.|You can view previously archived orders in Your Orders. To view previously archived orders: 1. Go to Your Orders. 2. Search for the relevant order, or filter for the date range that the order was originally purchased.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
