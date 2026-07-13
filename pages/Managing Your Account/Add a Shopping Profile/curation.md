#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|add_shopping_profile|Add a new shopping profile to personalize the shopping experience.|You can add up to five shopping profiles to personalize your experience:|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|edit_shopping_profile|Edit an existing shopping profile.|You can edit your profiles through the View option.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|remove_shopping_profile|Remove an existing shopping profile from the account.|If you reach the limit, you can remove a profile anytime. Select Remove profile and follow the on-screen prompts.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|ADD|Add intent `add_shopping_profile` to the taxonomy.|The page provides step-by-step instructions to create/add a new shopping profile on the account.|You can add up to five shopping profiles to personalize your experience:|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|ADD|Add intent `edit_shopping_profile` to the taxonomy.|The page explicitly supports the action of editing profiles via the View option.|You can edit your profiles through the View option.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=TE9UR1c1VsPhWeLGcl|ADD|Add intent `remove_shopping_profile` to the taxonomy.|The page provides instructions to remove an existing profile if needed.|If you reach the limit, you can remove a profile anytime. Select Remove profile and follow the on-screen prompts.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
