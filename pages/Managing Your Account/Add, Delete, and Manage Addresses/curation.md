#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|add_address|Add a new address for future orders.|To add a new address, select **Add address**. Enter the new address details. Add your delivery preferences and select **Add address**.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|edit_address|Edit details of an existing shipping address.|To edit an address, select **Edit** below the address. Change the address details and select **Update address**.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|delete_address|Delete an address from the account.|To delete an address, select **Remove** below the address. Select **Yes** to confirm. You can’t delete an address with pending Subscribe and Save orders. First, update the Subscribe and Save order with a different address.|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|set_default_address|Set a default shipping address for faster checkout.|To set a default shipping address, select **Set as Default** below the preferred address. Having a default address makes the checkout faster. You can change your default address anytime. Note that selecting a default shipping address won’t change your billing address.|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change_type|change_instruction|change_reason|change_evidence|is_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|MERGE|Merge candidate intents add_address, edit_address, delete_address, and set_default_address under manage_addresses|Grouping these related intents under a unified super-intent captures the overall customer activity of managing addresses on the account while preserving the specific self-service sub-tasks.|To add a new address, select **Add address**. Enter the new address details. Add your delivery preferences and select **Add address**... To edit an address, select **Edit** below the address. Change the address details and select **Update address**... To delete an address, select **Remove** below the address. Select **Yes** to confirm. You can’t delete an address with pending Subscribe and Save orders. First, update the Subscribe and Save order with a different address... To set a default shipping address, select **Set as Default** below the preferred address. Having a default address makes the checkout faster. You can change your default address anytime. Note that selecting a default shipping address won’t change your billing address.|No|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref_=hp_left_v4_sib&nodeId=GQT5HV6YYGNDSFNW|MERGE|Merge candidate intents add_address, edit_address, delete_address, and set_default_address under manage_addresses|Grouping these related intents under a unified super-intent captures the overall customer activity of managing addresses on the account while preserving the specific self-service sub-tasks.|To add a new address, select **Add address**. Enter the new address details. Add your delivery preferences and select **Add address**... To edit an address, select **Edit** below the address. Change the address details and select **Update address**... To delete an address, select **Remove** below the address. Select **Yes** to confirm. You can’t delete an address with pending Subscribe and Save orders. First, update the Subscribe and Save order with a different address... To set a default shipping address, select **Set as Default** below the preferred address. Having a default address makes the checkout faster. You can change your default address anytime. Note that selecting a default shipping address won’t change your billing address.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_INTENT_CANDIDATES and PAGE_INTENT_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_evidence|check_intent_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check_reasoning|check_change_proposal_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check_coverage|check_intent_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
