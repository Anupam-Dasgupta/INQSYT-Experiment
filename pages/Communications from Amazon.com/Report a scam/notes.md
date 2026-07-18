# Notes

## General Observations About the Page

The page details how customers and non-customers can report suspicious communications, fraud, phishing, or spoofing attempts claiming to be from Amazon. It provides tailored reporting wizard links based on what information (if any) was shared, a dedicated email address for non-account holders, and links to external or related reporting resources (e.g., FTC, brushing scams, gift card fraud).

---

## Navigation Structure

The page content is organized as follows:
1. Introduction: Serious stance on fraud/scams, prompt to report suspicious correspondence.
2. Shared Information Scenario Selector (Links):
   - No information shared
   - Shared Amazon account information
   - Shared Banking information
   - Given remote access to computer/devices
   - Shared other information
3. Non-Account Holder Reporting (Email channel to reportascam@amazon.com).
4. FTC Reporting Link (For phone calls and text messages/SMS).
5. Links to other help pages (Protect Your System, Report Suspicious Activity, Report Unsolicited Packages/Brushing, Common Gift Card Scams, Trustworthy Shopping).

---

## Page Quality Observations

The grouping of options based on what information was shared is logical and actionable. It clearly separates paths for account holders (wizard) and non-account holders (email). However, it relies heavily on redirecting users to other pages for related scam types.

---

## Missing Documentation

The page does not specify response times or details on what actions Amazon takes once a report is submitted, only stating that personal responses are not sent for reportascam@amazon.com emails.

---

## Missing Intents (Intentionally Excluded)

- `report_scam_to_ftc`: Excluded as a separate intent because it represents an external agency reporting recommendation and is a sub-flow of general reporting.
- `report_brushing_scam`, `report_gift_card_fraud`: Excluded as this page only links to other specialized help pages for those topics.

---

## Retrieval Challenges

Users may query with very specific scenarios like "I gave remote access to a caller" or "I forwarded a fake email to Amazon." Retrieval systems should ensure queries describing specific shared information types map successfully to this single reporting page.

---

## RAG Chunking Recommendations

We recommend dividing the content into three distinct chunks:
1. Account Holder Reporting: The introductory text and the five scenario links based on shared information.
2. Non-Account Holder Reporting: Instructions on sending suspicious communications to reportascam@amazon.com.
3. FTC and Related Resources: Redirection details to report fraud to the FTC and links to related scam topics.

---

## Intent Ambiguity Observations

There is potential overlap with "Identifying a scam," which focuses on verifying authenticity, whereas this page focuses on reporting. The line is clear: verification belongs in `verify_amazon_communication`, reporting in `report_amazon_scam`.

---

## Reusable Extraction Patterns

- "If you receive a correspondence you think may not be from Amazon, report it immediately."
- "If you don't have an Amazon account: You can still report..."

---

## Taxonomy Design Observations

A single unified intent `report_amazon_scam` is used to prevent over-granularity that would arise from splitting by scenario or by communication channel (e.g. phone, email, text).

---

## Edge Cases Noticed During Extraction

- Non-account holders are instructed to email reportascam@amazon.com as an attachment.
- The reporting wizard branches out based on whether the customer shared banking info, account credentials, or allowed remote access.

---

## Iteration 1 - Observations (2026-07-18)

- **Important extraction observations**: Strong wizard-based branching depending on user's exposure level (banking, remote access, account info, no info).
- **Approved taxonomy changes**: Added the intent `report_amazon_scam`.
- **Rejected taxonomy changes**: Proposing `report_scam_to_ftc` was rejected.
- **Retrieval observations**: Searches for phishing, fake emails, remote access, or spoofing should route to this page.
- **Taxonomy decisions**: Keeping a high-level intent (`report_amazon_scam`) is consistent with avoiding over-granularity.
- **Chunking observations**: Logical division matches reporting wizard, non-account email, and external resources.
- **Notable edge cases**: Reporting flow for non-account holders.
- **Lessons useful for future pages**: Keep the focus on Amazon's primary action (reporting to Amazon) and treat external redirection (like FTC) as secondary details.
