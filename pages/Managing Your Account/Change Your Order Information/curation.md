#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|change_order_information|Update order information, such as quantity, billing address, delivery address, or payment method, for orders that have not yet been dispatched.|You can update your order quantity, billing address, delivery address, payment method, and more on your orders that have not yet been dispatched by visiting the Orders section in Your Account. To change your order information: 1. Go to Your Orders. 2. Select Order Details for the order that you want to change. Then select Change next to the details that you want to update. 3. Follow the on-screen instructions.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|change_order_on_mobile|Change order information when using a mobile device, with desktop recommendations for address changes.|If you are on a mobile device, you can make changes to your payment method, but not to your address. You may find more options to change your order by visiting Amazon.com via desktop.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|update_third_party_order_address|Update the shipping address of an order shipped from a third-party seller.|To update the shipping address of an order from a third-party seller, go to Contact a Third-Party Seller.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|add_items_to_fresh_delivery|Add items to an upcoming Amazon Fresh, Whole Foods Market, or third-party merchant delivery.|To add items to an upcoming Amazon Fresh delivery, go to Modify your upcoming Amazon Fresh, Whole Foods Market, and Third Party Merchant Delivery.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|RENAME|Rename candidate intent `change_order_information` to `change_order_details`.|To avoid naming conflict with the proposed super-intent `change_order_information` while representing standard order updates.|To change your order information: 1. Go to Your Orders...|No|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|MERGE|Merge candidate intents `change_order_details` (renamed), `change_order_on_mobile`, `update_third_party_order_address`, and `add_items_to_fresh_delivery` under a new super-intent `change_order_information`.|These candidate intents represent specific sub-procedures, platform variations, or service-specific instructions for changing orders, and are best grouped under a single hierarchical super-intent.|Go to Your Orders ... If you are on a mobile device, you can make changes ... To update the shipping address of an order from a third-party seller ... To add items to an upcoming Amazon Fresh delivery ...|No|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|RENAME|Rename candidate intent `change_order_information` to `change_order_details`.|To avoid naming conflict with the proposed super-intent `change_order_information` while representing standard order updates.|To change your order information: 1. Go to Your Orders...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GSWAYSNV7RBSTND9|MERGE|Merge candidate intents `change_order_details` (renamed), `change_order_on_mobile`, `update_third_party_order_address`, and `add_items_to_fresh_delivery` under a new super-intent `change_order_information`.|These candidate intents represent specific sub-procedures, platform variations, or service-specific instructions for changing orders, and are best grouped under a single hierarchical super-intent.|Go to Your Orders ... If you are on a mobile device, you can make changes ... To update the shipping address of an order from a third-party seller ... To add items to an upcoming Amazon Fresh delivery ...|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
