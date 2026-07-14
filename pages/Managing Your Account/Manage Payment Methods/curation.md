#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|add_payment_method|Add a new payment method to the customer's Amazon account using the Your Payments section.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To add a payment method, select **Add a payment method**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|edit_payment_method|Edit card details or update the billing address of an existing payment method in Your Payments.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To edit a payment method, select the card you wish to edit. When the card opens, select **Edit**. You can update your billing address or update card details.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|remove_payment_method|Delete or remove an existing payment method from the customer's Amazon wallet.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To remove a payment method, select the card you wish to remove. When the card opens, select **Remove from wallet**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|add_payment_method_during_order|Add a new credit or debit card directly on the Select a Payment Method page during order checkout.|You can also add a new credit/debit card to your account while placing an order through the shopping cart; when on the **Select a Payment Method** page, choose **Add a credit or debit card** and enter your details.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|use_tap_to_pay|Add and use a contactless card to pay for an order using a compatible device and the Amazon app.|With Tap to Pay, you can add a contactless card to your wallet to pay for your order. Use the Amazon app with a compatible device for Tap to Pay transactions.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|ADD|Add intent `add_payment_method` to the taxonomy.|The page provides step-by-step instructions to add a payment method in Your Payments.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To add a payment method, select **Add a payment method**.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|ADD|Add intent `edit_payment_method` to the taxonomy.|The page provides step-by-step instructions to edit card details or update billing address in Your Payments.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To edit a payment method, select the card you wish to edit. When the card opens, select **Edit**. You can update your billing address or update card details.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|ADD|Add intent `remove_payment_method` to the taxonomy.|The page provides step-by-step instructions to remove a contactless card/wallet entry.|To manage your payment methods: 1. In **Your Account**, select **Your Payments**. 2. Choose one of the following: * To remove a payment method, select the card you wish to remove. When the card opens, select **Remove from wallet**.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|ADD|Add intent `add_payment_method_during_order` to the taxonomy.|The page describes how to add a credit/debit card during the checkout phase.|You can also add a new credit/debit card to your account while placing an order through the shopping cart; when on the **Select a Payment Method** page, choose **Add a credit or debit card** and enter your details.|REJECTED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GNQFBWDZJN838JZF|ADD|Add intent `use_tap_to_pay` to the taxonomy.|The page explains how to use Tap to Pay to pay for orders using compatible devices.|With Tap to Pay, you can add a contactless card to your wallet to pay for your order. Use the Amazon app with a compatible device for Tap to Pay transactions.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
