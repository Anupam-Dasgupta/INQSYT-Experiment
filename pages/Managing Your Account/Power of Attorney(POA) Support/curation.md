#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TCouxVXY0LmWAy8NEi|request_poa_support|Request Amazon's Power of Attorney (POA) support via email to share account information or handle an account on behalf of the account owner when you don't have access to the account.|To protect customer data, we can only share account information or handle an account when the requester is the authorized person. ... To continue with your request, attach the listed documentation and email it to our dedicated support team: **poa-support@amazon.com**.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TCouxVXY0LmWAy8NEi|ADD|Add `request_poa_support` intent to support requesting Power of Attorney (POA) assistance via email.|A new Power of Attorney (POA) support channel is introduced by this help page, which is not covered by any existing taxonomy intents.|To continue with your request, attach the listed documentation and email it to our dedicated support team: **poa-support@amazon.com**.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
