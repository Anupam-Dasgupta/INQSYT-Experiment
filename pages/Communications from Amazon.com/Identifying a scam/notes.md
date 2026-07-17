# Notes

## General Observations About the Page

The page describes impersonation scams and outlines warning signs (red flags) to help customers distinguish legitimate Amazon communications from scams. It also introduces Amazon's communication verification tools and channels (such as `Verify a call or message` button and the `verify@amazon.com` email address).

---

## Navigation Structure

The page is structured as follows:
1. Header: "Identifying a scam"
2. Description of impersonation scams.
3. List of scam warning signs / red flags (urgency, personal info, off-site transactions, gift card payments, etc.).
4. Steps and links to verify a call or message (online tool and email forwarding).
5. Section on reporting a scam (Report a scam button, reportascam email for non-customers).

---

## Page Quality Observations

The warning indicators listed are comprehensive. Providing active digital tools (the online verification button and dedicated emails) is critical to customer security.

---

## Missing Documentation

The page does not explain response timeframes for verifying emails sent to `verify@amazon.com`.

---

## Missing Intents (Intentionally Excluded)

- `report_amazon_scam`: Rejections recorded. The user explicitly chose to exclude the reporting intent from this page's taxonomy.

---

## Retrieval Challenges

Customers might search using phrases like "is this email from Amazon", "suspicious text message verify", "fake call from Amazon", or "forward phishing email". All of these must map to the verification intent.

---

## RAG Chunking Recommendations

We recommend splitting the document into three chunks:
1. Impersonation Scams & Red Flags: Explains what a scam is and lists the red flags.
2. Verification Tools: Steps and tools to verify if a message is legitimate.
3. Reporting Scams: Explains how and where to report suspicious activity.

---

## Intent Ambiguity Observations

There could be overlap with avoiding general payment scams, but this page is focused specifically on *verifying* communications claiming to originate from Amazon.

---

## Reusable Extraction Patterns

- "If you've received a suspicious email, call, or message..."
- "Verify it before taking action..."
- "Amazon will not ask you for..."

---

## Taxonomy Design Observations

The user rejected the separate intent for reporting scams (`report_amazon_scam`) for this page, keeping the taxonomy focused solely on communication verification (`verify_amazon_communication`).

---

## Edge Cases Noticed During Extraction

- Non-customers can report scams by emailing `reportascam@amazon.com`.
- Scammers use high-pressure tactics or False Urgency to bypass typical validation steps.

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Strong distinction between verification (approved) and reporting (rejected) intent boundaries.
- **Approved taxonomy changes**: Added the intent `verify_amazon_communication`.
- **Rejected taxonomy changes**: Proposing `report_amazon_scam` was rejected.
- **Retrieval observations**: Users checking authenticity will search for verification patterns.
- **Taxonomy decisions**: Keeping the focus narrow on verification is preferred by the user.
- **Chunking observations**: Distinct segments exist for diagnosing/identifying (red flags), verifying (tools), and reporting.
- **Notable edge cases**: Reporting channels for non-account holders.
- **Lessons useful for future pages**: Rejection of secondary intents (like reporting when verification is the primary theme) shows a preference for concise page-level intents.
