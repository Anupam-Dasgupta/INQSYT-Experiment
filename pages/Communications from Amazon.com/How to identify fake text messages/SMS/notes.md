# Notes

## General Observations About the Page

- The page covers techniques for customers to identify fake/phishing text messages (SMS) claiming to be from Amazon.
- Explains key indicators such as unrecognized sender numbers, unexpected order references, and links with typos/IPs.
- Includes a key policy statement: Amazon never requests personal information, payment details, gift card codes, or phone calls via SMS.

## Navigation Structure

- High-level list of tips for SMS verification.
- Links to related help topics: Identifying a scam, How to identify fake emails, How to identify fake phone calls, How to identify fake websites, Report a scam.

## Page Quality Observations

- The document is clear and readable.
- Direct links are provided for verification.
- Includes advice on order history verification.

## Missing Documentation

- No clear visual example of fraudulent SMS (the text mentions an example but it doesn't render text-based content).

## Missing Intents (Intentionally Excluded)

- `check_order_history`: Excluded because checking order history is a verification action performed on the order history page, not a direct capability of this page.
- `report_suspicious_sms` / `report_amazon_scam`: Excluded because reporting scams is a distinct user goal supported by the dedicated "Report a scam" page.

## Retrieval Challenges

- High conceptual overlap with other fraud pages (emails, websites, phone calls) due to similar indicators.

## RAG Chunking Recommendations

- Chunk 1: Phone numbers, unexpected order text, and Amazon's non-request policies.
- Chunk 2: Identifying phishing links and actions to take (scam reporting and order checking).

## Intent Ambiguity Observations

- Ambiguity may occur between general scam verification and SMS-specific verification.

## Reusable Extraction Patterns

- Cues like "Scammers may send text messages claiming to be Amazon. These aren't from Amazon if they include:" and "Important Note: Amazon will never ask you...".

## Taxonomy Design Observations

- Kept the taxonomy simple by including only the main intent `identify_fake_sms` per user instructions, discarding the secondary candidates.

## Edge Cases Noticed During Extraction

- A fraudulent SMS example is present on the page but appears to lack text representation in the text scrape.

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded `identify_fake_sms`, `check_order_history`, and `report_suspicious_sms`.
- The user approved `identify_fake_sms` and rejected the others to maintain a focused taxonomy.
- The final taxonomy is documented in taxonomy.md.
