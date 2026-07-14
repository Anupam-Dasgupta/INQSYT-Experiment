#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TzcJJiVFnIi3pG2yDA|request_bereavement_support|Request Amazon's bereavement support via email to close/deactivate an account, stop subscriptions/deliveries, or request account information.|For support regarding these topics, please email **bereavement-support-cs@amazon.com**. Be sure to include the death certificate and the email or phone number associated with the account. ... Once you've gathered the required documentation: Email it to **bereavement-support-cs@amazon.com**.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TzcJJiVFnIi3pG2yDA|ADD|Add intent `request_bereavement_support` to the taxonomy.|The page details how users can request account information, closure, or changes (such as terminating subscriptions, stopping recurring deliveries, or deactivating an account) via email to Amazon's bereavement support team.|For support regarding these topics, please email **bereavement-support-cs@amazon.com**. Be sure to include the death certificate and the email or phone number associated with the account. ... Once you've gathered the required documentation: Email it to **bereavement-support-cs@amazon.com**.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
