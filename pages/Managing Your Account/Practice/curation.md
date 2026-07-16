#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|close_amazon_account|Submit a request to permanently close the Amazon account and delete personal information.|You can submit a request for us to close your Amazon account and delete your personal information permanently.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|request_account_closure_as_non_holder|Request account closure and data deletion via email if not having an account or acting as an authorized agent.|If you do not have an account, or if you are an authorized agent under applicable state law, email us.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change\_type|change\_instruction|change\_reason|change\_evidence|is\_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|MERGE|Merge candidate intents close_amazon_account and request_account_closure_as_non_holder into close_account.|Both intents represent the overarching goal of requesting the closure of the Amazon account and deletion of personal data, whether the user currently holds an active login account or not.|You can submit a request for us to close your Amazon account and delete your personal information permanently. / If you do not have an account, or if you are an authorized agent under applicable state law, email us.|No|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
