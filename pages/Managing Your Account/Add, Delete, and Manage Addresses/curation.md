#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|add_address|Add a new delivery address to the customer's account for future orders.|To add a new address, select **Add address**. Enter the new address details. Add your delivery preferences and select **Add address**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|edit_address|Edit an existing address in the customer's account.|To edit an address, select **Edit** below the address. Change the address details and select **Update address**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|delete_address|Delete a delivery address from the customer's account.|To delete an address, select **Remove** below the address. Select **Yes** to confirm.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|set_default_address|Set a preferred delivery address as the default shipping address.|To set a default shipping address, select **Set as Default** below the preferred address.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|ADD|Add intent `add_address` to the taxonomy.|The page provides instructions for adding a new delivery address.|To add a new address, select **Add address**. Enter the new address details. Add your delivery preferences and select **Add address**.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|ADD|Add intent `edit_address` to the taxonomy.|The page provides instructions for editing an existing address.|To edit an address, select **Edit** below the address. Change the address details and select **Update address**.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|ADD|Add intent `delete_address` to the taxonomy.|The page provides instructions for deleting an existing address.|To delete an address, select **Remove** below the address. Select **Yes** to confirm.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GQT5HV6YYGNDSFNW|ADD|Add intent `set_default_address` to the taxonomy.|The page provides instructions for setting a preferred address as the default shipping address.|To set a default shipping address, select **Set as Default** below the preferred address.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
