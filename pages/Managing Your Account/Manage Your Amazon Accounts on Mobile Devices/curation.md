#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G5LD93RTW3MMDKCR|access_switch_accounts|Access Switch Accounts in the Amazon shopping app settings to add, remove, or switch between Amazon accounts on a mobile device.|To manage your Amazon account on a mobile device: 1. In your **Amazon shopping app**, go to **Menu**. 2. Go to **Settings** and select **Switch Accounts**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G5LD93RTW3MMDKCR|deregister_device|Deregister a device that is no longer accessible through the Manage Your Content and Devices page to sign out of it.|If you need to sign out from a device you no longer have access to, sign into your **Amazon account** on a desktop or mobile browser, and visit the **Manage Your Content and Devices** page. Under the **Devices** tab, select your device in the list, and select **Deregister**.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G5LD93RTW3MMDKCR|ADD|Add intent `access_switch_accounts` to the taxonomy.|The page provides instructions to access Switch Accounts settings in the Amazon app to add, remove, or switch accounts.|To manage your Amazon account on a mobile device: 1. In your **Amazon shopping app**, go to **Menu**. 2. Go to **Settings** and select **Switch Accounts**.|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=G5LD93RTW3MMDKCR|ADD|Add intent `deregister_device` to the taxonomy.|The page provides instructions to remotely sign out of a device by deregistering it on the Manage Your Content and Devices page.|If you need to sign out from a device you no longer have access to, sign into your **Amazon account** on a desktop or mobile browser, and visit the **Manage Your Content and Devices** page. Under the **Devices** tab, select your device in the list, and select **Deregister**.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|
