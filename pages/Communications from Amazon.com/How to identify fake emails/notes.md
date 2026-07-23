# Notes

## General Observations About the Page

- The page covers techniques for customers to identify fake/phishing emails claiming to be from Amazon.
- Key indicators discussed include check Message Center, check sender email domains, check for typos/errors, verify links, and inspect attachments.

## Navigation Structure

- High-level list of tips for email verification.
- Links to related help topics: Identifying a scam, How to identify fake text messages/SMS, How to identify fake phone calls, How to identify fake websites, Report a scam.

## Page Quality Observations

- The document is clear and readable.
- It includes repeated advice about checking order history for unrecognized orders.

## Missing Documentation

- Technical details on BIMI (Brand Indicators for Message Identification) or standard email authentication (SPF, DKIM, DMARC) are omitted for simplicity.

## Missing Intents (Intentionally Excluded)

- `check_order_history`: Excluded because checking order history is a verification action performed on the order history page, not a direct capability of this page.
- `report_suspicious_email` / `report_amazon_scam`: Excluded because reporting scams is a distinct user goal supported by the dedicated "Report a scam" page.

## Retrieval Challenges

- High conceptual overlap with other communication fraud pages (SMS, phone, websites) because they share common indicators (such as typos, links).

## RAG Chunking Recommendations

- Chunk 1: Check Message Center and sender address (including BIMI).
- Chunk 2: Verification of links and attachments.

## Intent Ambiguity Observations

- Ambiguity may arise between general scam verification and email-specific verification.

## Reusable Extraction Patterns

- Format checks: "To check whether an [X] is from Amazon:" and "If you received correspondence regarding [Y]...".

## Taxonomy Design Observations

- Kept the taxonomy simple by including only the main intent `identify_fake_emails` per user instructions, discarding the secondary candidates.

## Edge Cases Noticed During Extraction

- The page redirects customers to "Your Orders" if they receive notifications for orders they did not place.

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded `identify_fake_emails`, `check_order_history`, and `report_suspicious_email`.
- The user approved `identify_fake_emails` and rejected the others to maintain a focused taxonomy.
- The final taxonomy is documented in taxonomy.md.
