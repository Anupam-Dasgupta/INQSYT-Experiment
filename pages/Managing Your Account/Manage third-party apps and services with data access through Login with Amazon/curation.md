#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GSNRZP4F7NYG36N6|remove_third_party_access|Remove the connection between a third-party app or service and the customer's Amazon account to stop it from accessing data.|To remove third party access: 1. Make sure you're signed into the **Amazon Account**. 2. Go to **Your Account** > **Manage your data** > **Manage apps & services with data access**. 3. Select **Remove** next to the app or service whose connection you want to remove.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GSNRZP4F7NYG36N6|ADD|Add intent `remove_third_party_access` to the taxonomy.|The page provides step-by-step instructions to remove a third-party app or service data access connection to the Amazon account.|To remove third party access: 1. Make sure you're signed into the **Amazon Account**. 2. Go to **Your Account** > **Manage your data** > **Manage apps & services with data access**. 3. Select **Remove** next to the app or service whose connection you want to remove.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
