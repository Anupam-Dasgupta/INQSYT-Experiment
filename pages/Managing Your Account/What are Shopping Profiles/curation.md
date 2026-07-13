#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=T0MhVXZmePWB0G6ttw|understand_shopping_profiles|Understand what shopping profiles are and how they personalize the shopping experience on shared accounts.|Shopping profiles give adults and teens in certain jurisdictions who share an Amazon account a more personalized experience. Profiles use activities like searches and browsing history to give tailored recommendations to the shopper.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=T0MhVXZmePWB0G6ttw|understand_shopping_profile_privacy|Understand the privacy implications and limitations of setting up shopping profiles on a shared account.|Setting up shopping profiles will not enable any additional privacy between customers who share accounts. Activities that take place within the account will continue to be the responsibility of the account holder.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=T0MhVXZmePWB0G6ttw|ADD|Add intent `understand_shopping_profiles` to the taxonomy.|The page provides general and introductory information explaining what shopping profiles are and how they personalize the account.|Shopping profiles give adults and teens in certain jurisdictions who share an Amazon account a more personalized experience. Profiles use activities like searches and browsing history to give tailored recommendations to the shopper.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=T0MhVXZmePWB0G6ttw|ADD|Add intent `understand_shopping_profile_privacy` to the taxonomy.|The page explicitly details the lack of additional privacy/separation between users sharing an account.|Setting up shopping profiles will not enable any additional privacy between customers who share accounts. Activities that take place within the account will continue to be the responsibility of the account holder.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
