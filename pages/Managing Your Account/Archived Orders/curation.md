#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G7882F7JTSV9N5BS|view_archived_orders|View previously archived orders in the customer's account.|To view previously archived orders: 1. Go to **Your Orders**. 2. Search for the relevant order, or filter for the date range that the order was originally purchased.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G7882F7JTSV9N5BS|ADD|Add intent `view_archived_orders` to the taxonomy.|The page provides instructions for viewing previously archived orders in order history by searching or filtering.|To view previously archived orders: 1. Go to **Your Orders**. 2. Search for the relevant order, or filter for the date range that the order was originally purchased.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
