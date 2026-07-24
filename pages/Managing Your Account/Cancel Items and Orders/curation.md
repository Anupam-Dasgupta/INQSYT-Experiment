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
