#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TzQnumpZFz1aqEoHiK|check_credit_and_benefit_balances|Check promotional credits and benefit balances in the customer's account.|To check your promotional credits and balance: 1. Go to **Your Account**. 2. Select **Your credit & benefit balances**. You can also go directly to **Your credit & benefit balances**.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TzQnumpZFz1aqEoHiK|ADD|Add intent `check_credit_and_benefit_balances` to the taxonomy.|The page provides instructions for checking promotional credits and balance in the customer's account.|To check your promotional credits and balance: 1. Go to **Your Account**. 2. Select **Your credit & benefit balances**. You can also go directly to **Your credit & benefit balances**.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
