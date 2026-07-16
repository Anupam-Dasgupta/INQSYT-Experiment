#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GBDB29JHRPFBDVYV|understand_account_closure_consequences|Understand the consequences and global impacts of closing an Amazon account, including the loss of access to associated services and features.|Once your account has been closed, all products and services accessed through your account will no longer be available to you, across any Amazon site globally. / Closing your account permanently means you won't have access to the features associated with your closed account, including: [features]|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GBDB29JHRPFBDVYV|understand_pre_closure_recommendations|Understand the recommended actions to take before requesting account closure, such as downloading uploaded content and invoices.|We recommend you download any of the content you uploaded to one of our services (such as Amazon Photos), before closing your account. We also recommend downloading any invoices you might need.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change\_type|change\_instruction|change\_reason|change\_evidence|is\_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GBDB29JHRPFBDVYV|MERGE|Merge candidate intents understand_account_closure_consequences and understand_pre_closure_recommendations into understand_account_closure_consequences.|Both topics represent the informational goal of understanding the implications, consequences, and preparatory recommendations for closing an Amazon account, which are tightly coupled in the user journey.|We recommend you download any of the content you uploaded... before closing your account. / Once your account has been closed, all products and services accessed through your account will no longer be available...|No|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
