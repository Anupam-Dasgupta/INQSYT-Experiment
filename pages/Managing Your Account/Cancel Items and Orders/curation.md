#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|cancel_order|Cancel physical items or an entire order that has not entered the shipping process yet.|To cancel an order that has not entered the shipping process, follow these steps: 1. Go to Your Orders. 2. Find the order that you want to cancel and select View or edit order. 3. Select Cancel items. 4. Check box of the item that you want to cancel from the order. To cancel the entire order, select all the items. 5. Choose a reason for the cancellation and select Request cancellation.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|view_canceled_orders|View a history of previously canceled orders.|For a history of your cancelled orders, visit Your Orders under Canceled Orders.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|refuse_shipped_package|Refuse or return a shipped package when the order has already entered shipping and cannot be canceled.|If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|contact_third_party_seller|Contact a third-party seller to request cancellation of an order that cannot be changed.|If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|MERGE|Merge candidate intents `cancel_order`, `view_canceled_orders`, `refuse_shipped_package`, and `contact_third_party_seller` under a new super-intent `cancel_items_and_orders`.|These candidate intents all represent specific actions and procedures related to cancelling orders, viewing cancellation history, or handling orders that cannot be canceled, which are best grouped under a single order-cancellation-focused super-intent.|You can cancel physical items or orders that haven't entered the shipping process yet. ... For a history of your cancelled orders, visit Your Orders under Canceled Orders. ... If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center. ... If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|No|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|MERGE|Merge candidate intents `cancel_order`, `view_canceled_orders`, `refuse_shipped_package`, and `contact_third_party_seller` under a new super-intent `cancel_items_and_orders`.|These candidate intents all represent specific actions and procedures related to cancelling orders, viewing cancellation history, or handling orders that cannot be canceled, which are best grouped under a single order-cancellation-focused super-intent.|You can cancel physical items or orders that haven't entered the shipping process yet. ... For a history of your cancelled orders, visit Your Orders under Canceled Orders. ... If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center. ... If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|DELETE|Delete candidate intents `refuse_shipped_package` and `contact_third_party_seller`.|The user requested to combine these two intents into a single intent for handling orders that cannot be canceled.|N/A|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `handle_uncancelable_order` under super-intent `cancel_items_and_orders`.|Request help with an order that can no longer be canceled, including refusing or returning an Amazon-shipped package or contacting a third-party seller.|If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center. If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|MERGE|Merge candidate intents `cancel_order` and `view_canceled_orders` along with new intent `handle_uncancelable_order` under super-intent `cancel_items_and_orders`.|Organize all cancel-related intents under a single super-intent.|To cancel an order that has not entered the shipping process... For a history of your cancelled orders, visit Your Orders under Canceled Orders. If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center. If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
