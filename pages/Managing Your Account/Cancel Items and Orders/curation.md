#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|cancel_amazon_order|Cancel physical items or orders shipped and sold or fulfilled by Amazon that haven't entered the shipping process.|You can cancel physical items or orders that haven't entered the shipping process yet.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|cancel_third_party_seller_order|Cancel orders sold and shipped by a third-party seller.|Orders sold and shipped by a third-party seller can typically be canceled within one business day.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|return_shipped_package|Refuse or return a package using the Online Returns Center if the order has shipped from Amazon and cannot be changed.|If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center (https://www.amazon.com/returns).|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|contact_third_party_seller|Contact a third-party seller when an order shipped directly from them cannot be changed.|If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|view_cancelled_orders|View the history of cancelled orders in Your Orders under Canceled Orders.|For a history of your cancelled orders, visit Your Orders (https://www.amazon.com/gp/css/your-orders-access) under Canceled Orders.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `cancel_amazon_order` to the taxonomy.|The page supports cancelling physical items or orders shipped and sold or fulfilled by Amazon.|You can cancel physical items or orders that haven't entered the shipping process yet.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `cancel_third_party_seller_order` to the taxonomy.|The page supports cancelling orders shipped by third-party sellers.|Orders sold and shipped by a third-party seller can typically be canceled within one business day.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `return_shipped_package` to the taxonomy.|The page explains how to refuse or return a package if the order has already shipped and cannot be changed.|If your order is shipped directly from Amazon and can't be changed, refuse or return the package using our Online Returns Center (https://www.amazon.com/returns).|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `contact_third_party_seller` to the taxonomy.|The page explains that the user should contact the third-party seller if an order has shipped from them and cannot be changed.|If your order is shipped directly from a third-party seller and can't be changed, contact the seller.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?nodeId=GSL37WQTJZUYA9QE|ADD|Add intent `view_cancelled_orders` to the taxonomy.|The page provides instructions to view the history of cancelled orders.|For a history of your cancelled orders, visit Your Orders (https://www.amazon.com/gp/css/your-orders-access) under Canceled Orders.|REJECTED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
