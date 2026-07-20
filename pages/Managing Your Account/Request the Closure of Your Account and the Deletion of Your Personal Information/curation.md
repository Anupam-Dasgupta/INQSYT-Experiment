#### PAGE_INTENT_CANDIDATES

|url|intent_name|intent_description|evidence|
|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|request_account_closure_and_data_deletion|Submit a request to permanently close an Amazon account and delete personal information.|Follow these steps to submit a request to close your Amazon account and delete your personal information: 1. Go to Close Your Amazon Account. 2. Sign into the account you want to close. 3. Review the products and services associated with your account. 4. If you still wish to proceed, you can select a reason in the drop-down menu. Then select the box next to **Yes, I want to permanently close my Amazon account and delete my data**. To complete the closure, select **Close my Account**.|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|request_closure_and_deletion_without_account|Request account closure or data deletion via email if the customer does not have an account or is an authorized agent.|If you do not have an account, or if you are an authorized agent under applicable state law, [email us](mailto:us-datarequest@amazon.com).|

#### PAGE_INTENT_CHANGE_PROPOSALS

|url|change\_type|change\_instruction|change\_reason|change\_evidence|is\_approved|
|-|-|-|-|-|-|
|https://www.amazon.com/gp/help/customer/display.html?ref\_=hp\_left\_v4\_sib\&nodeId=GDK92DNLSGWTV6MP|MERGE|Merge candidate intents request_account_closure_and_data_deletion and request_closure_and_deletion_without_account into close_account.|Both candidate intents describe different pathways for the same customer goal of account closure and personal data deletion (online vs. email), and can be grouped under the broader super-intent close_account.|You can submit a request for us to close your Amazon account and delete your personal information permanently. / If you do not have an account, or if you are an authorized agent under applicable state law, email us (mailto:us-datarequest@amazon.com).|No|
