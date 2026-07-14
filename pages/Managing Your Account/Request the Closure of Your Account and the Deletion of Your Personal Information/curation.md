#### PAGE_INTENT_CANDIDATES

|url|intent\_name|intent\_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|close_amazon_account|Submit a request to permanently close the Amazon account and delete personal information.|You can submit a request for us to close your Amazon account and delete your personal information permanently.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|request_account_closure_as_non_holder|Request account closure and data deletion via email if not having an account or acting as an authorized agent.|If you do not have an account, or if you are an authorized agent under applicable state law, email us.|

#### USER_APPROVAL_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|MERGE|Merge candidate intents close_amazon_account and request_account_closure_as_non_holder into close_account.|Both intents represent the overarching goal of requesting the closure of the Amazon account and deletion of personal data, whether the user currently holds an active login account or not.|You can submit a request for us to close your Amazon account and delete your personal information permanently. / If you do not have an account, or if you are an authorized agent under applicable state law, email us.|APPROVED|

#### REVIEW_VALIDATION_CHECKS

|check\_type|check\_name|check\_instruction|is\_approved|
|-|-|-|-|
|check\_format|check\_output\_formats|Verify that PAGE\_INTENT\_CANDIDATES and PAGE\_INTENT\_CHANGE\_PROPOSALS conform to their expected schemas.|Yes|
|check\_evidence|check\_intent\_grounding|Verify that every candidate intent and every proposed change is supported by evidence from the source page.|Yes|
|check\_reasoning|check\_change\_proposal\_reasons|Verify that every proposed MERGE, SPLIT, RENAME, ADD, or DELETE is reasonable and clearly justified.|Yes|
|check\_coverage|check\_intent\_coverage|Verify that no obvious customer goal or refinement proposal directly supported by the page has been omitted.|Yes|

#### PAGE_CHUNK_CANDIDATES

|url|chunk_id|supported_intents|candidate_chunk|chunk_boundary_justification|evidence|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|account_closure_procedure|close_account|### Request the Closure of Your Account and the Deletion of Your Personal Information\<br\>\<br\>You can submit a request for us to close your Amazon account and delete your personal information permanently.\<br\>\<br\>#### Submit A Request To Close Your Amazon Account And Delete Your Personal Information:\<br\>\<br\>Follow these steps to submit a request to close your Amazon account and delete your personal information:\<br\>\<br\>1.  Go to [Close Your Amazon Account](https://www.amazon.com/privacy/data-deletion).\<br\>2.  Sign into the account you want to close.\<br\>3.  Review the products and services associated with your account.\<br\>4.  If you still wish to proceed, you can select a reason in the drop-down menu. Then select the box next to \*\*Yes, I want to permanently close my Amazon account and delete my data\*\*. To complete the closure, select \*\*Close my Account\*\*.\<br\>5.  A confirmation notification will be sent to the email address associated with your account or via text message. You’ll need to reply within five days to verify your request.|This block contains the main overview and step-by-step instructions for submitting an online request to close an Amazon account and delete personal data, forming a coherent procedural unit.|You can submit a request for us to close your Amazon account and delete your personal information permanently. / Follow these steps to submit a request to close your Amazon account and delete your personal information:|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|account_closure_consequences|close_account|#### Consequences of Closing Your Account\<br\>\<br\>\*   Once your account has been closed, all products and services accessed through your account will no longer be available to you, across any Amazon site globally. For example, submitting your account closure request through this website will also close your account on [amazon.com](https://www.amazon.com), [amazon.fr](https://www.amazon.fr), [amazon.com.mx](https://www.amazon.com.mx), and all other global sites that use the same credentials to access services and products offered through those sites.\<br\>\*   Once your Amazon account is closed, you will not be able to access and manage any of your business accounts – such as Seller accounts, Brand Registry accounts, or Advertising accounts – as well as other products and services included in the closed accounts.\<br\>\*   Once your account is closed, it is no longer accessible to you and it cannot be restored. If you decide later that you want to start ordering from us again, or if you would like to use website features that require an account, you\'ll need to create a new account. To learn more, visit [What Happens When I Close My Account?](https://www.amazon.com/gp/help/customer/display.html?nodeId=GBDB29JHRPFBDVYV)|This block describes the specific global and commercial consequences of account closure, separating policy disclosures from the active procedure.|#### Consequences of Closing Your Account|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|account_closure_special_cases|close_account|#### Multiple Accounts\<br\>\<br\>If you have multiple accounts, you need to follow the listed steps for each of the accounts. This ensures that we have the correct authority to take action on each account you wish to close.\<br\>\<br\>#### Additional Support\<br\>\<br\>\*   If you are experiencing issues with logging into the account you wish to close, go to [Why Can\'t I Log into My Account?](https://www.amazon.com/gp/help/customer/display.html?nodeId=GAM5QWMWMTFCHEQT) for further assistance.\<br\>\*   If you do not have an account, or if you are an authorized agent under applicable state law, [email us](mailto:us-datarequest@amazon.com).|This block groups supplementary support guidelines, including managing multiple accounts, troubleshooting login issues, and email submission options for non-account holders/agents.|#### Multiple Accounts / #### Additional Support|

#### USER_APPROVAL_CHUNK_TABLE

|url|change_type|change_instruction|change_reason|change_evidence|human_approval|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|ADD|Add candidate chunk `account_closure_procedure`.|To index the primary online procedure for closing an Amazon account.|### Request the Closure of Your Account...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|ADD|Add candidate chunk `account_closure_consequences`.|To index the consequences and global impacts of account closure.|#### Consequences of Closing Your Account...|APPROVED|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|ADD|Add candidate chunk `account_closure_special_cases`.|To index instructions for multiple accounts and non-account holder support channels.|#### Multiple Accounts...|APPROVED|

#### CHUNKING_VALIDATION_CHECKS

|check_type|check_name|check_instruction|is_approved|
|-|-|-|-|
|check_format|check_output_formats|Verify that PAGE_CHUNK_CANDIDATES and PAGE_CHUNK_CHANGE_PROPOSALS conform to their expected schemas.|Yes|
|check_coverage|check_intent_chunk_coverage|Verify that every intent in PAGE_INTENT_FINAL is supported by one or more candidate chunks.|Yes|
|check_evidence|check_chunk_grounding|Verify that every candidate chunk and every proposed chunking change is supported by evidence from the source page.|Yes|
|check_boundaries|check_chunk_boundaries|Verify that chunk boundaries preserve coherent semantic units and do not unnecessarily split procedures or combine unrelated customer goals.|Yes|
|check_reasoning|check_chunk_change_reasons|Verify that every proposed ADD, DELETE, MERGE, SPLIT, MODIFY, or REASSIGN operation is reasonable and clearly justified.|Yes|
|check_retrieval|check_retrieval_quality|Verify that the proposed chunking supports effective semantic retrieval for the approved intents.|Yes|
