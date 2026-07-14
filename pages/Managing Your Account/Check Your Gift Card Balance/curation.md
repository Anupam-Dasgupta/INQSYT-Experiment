#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|check_gift_card_balance|Check the current balance of Amazon.com Gift Cards stored in the customer's account.|To find your Amazon.com Gift Card balance in Your Account: 1. Go to **Your Account**. 2. Select **Gift cards** and check the balance on any of your **Amazon.com** Gift Cards.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|check_unvalued_physical_gift_card|Check the value of a physical Amazon.com Gift Card that does not have the value printed on it using Your Orders.|Some physical gift cards bought from **Amazon.com** don't come with values printed on them. In this case, you can check the value by going to **Your Orders**. In **Your Orders**, find the gift card order, and compare the 16-digit serial number (located beside the gift card amount) in the order details to the serial number on the back of the gift card.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|view_gift_card_transactions|View the transaction history and changes to the Amazon.com Gift Card balance.|You can check all changes to your balance in the transaction section of your **Balance Page**, including order IDs or serial numbers.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|ADD|Add intent `check_gift_card_balance` to the taxonomy.|The page provides instructions to find and check the Amazon.com Gift Card balance in Your Account.|To find your Amazon.com Gift Card balance in Your Account: 1. Go to **Your Account**. 2. Select **Gift cards** and check the balance on any of your **Amazon.com** Gift Cards.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|ADD|Add intent `check_unvalued_physical_gift_card` to the taxonomy.|The page provides a dedicated procedure to check the value of physical gift cards that do not have printed values using Your Orders.|Some physical gift cards bought from **Amazon.com** don't come with values printed on them. In this case, you can check the value by going to **Your Orders**. In **Your Orders**, find the gift card order, and compare the 16-digit serial number (located beside the gift card amount) in the order details to the serial number on the back of the gift card.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GJDWQ6WX5MKQP3E6|ADD|Add intent `view_gift_card_transactions` to the taxonomy.|The page explicitly supports checking changes to the balance in the transaction section of the Balance Page.|You can check all changes to your balance in the transaction section of your **Balance Page**, including order IDs or serial numbers.|REJECTED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
