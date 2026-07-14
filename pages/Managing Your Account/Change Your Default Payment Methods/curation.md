#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G4MVXVJB8QKE7MLW|change_default_payment_method|Select or change the default payment method in the customer's account wallet.|How to change your default payment method: 1. Go to **Your Wallet**. ... 2. Select the payment method to set as the default. Select **Edit**. 3. Select the box **Set as default payment method**. ... 4. Select **Save**.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G4MVXVJB8QKE7MLW|ADD|Add intent `change_default_payment_method` to the taxonomy.|The page provides instructions for selecting or changing the default payment method in the wallet.|How to change your default payment method: 1. Go to **Your Wallet**. ... 2. Select the payment method to set as the default. Select **Edit**. 3. Select the box **Set as default payment method**. ... 4. Select **Save**.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
