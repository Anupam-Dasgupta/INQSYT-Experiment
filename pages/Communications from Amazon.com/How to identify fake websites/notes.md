# Notes

## General Observations About the Page

- The page covers techniques for customers to identify fake/phishing websites claiming to be from Amazon.
- Explains red flags including IP-based URLs, URL spelling mistakes, mismatched link destinations when hovered, and the necessity of secure 'https://' connections.

## Navigation Structure

- High-level list of tips for website verification.
- Links to related help topics: Identifying a scam, How to identify fake emails, How to identify fake text messages/SMS, How to identify fake phone calls, Report a scam.

## Page Quality Observations

- The document is clear and readable.
- Direct links are provided for verification.
- Includes advice on order history verification.

## Missing Documentation

- No clear visual examples of fake checkout interfaces or similar pages.

## Missing Intents (Intentionally Excluded)

- `check_order_history`: Excluded because checking order history is a verification action performed on the order history page, not a direct capability of this page.
- `report_suspicious_website` / `report_amazon_scam`: Excluded because reporting scams is a distinct user goal supported by the dedicated "Report a scam" page.

## Retrieval Challenges

- High conceptual overlap with other fraud pages (emails, SMS, phone calls) due to similar indicators.

## RAG Chunking Recommendations

- Chunk 1: Red flags (IP-based URLs, URL spelling errors, hovering links).
- Chunk 2: Safety practices (checking HTTPS, verifying links, order history checks).

## Intent Ambiguity Observations

- Ambiguity may occur between general scam verification and website-specific verification.

## Reusable Extraction Patterns

- Cues like "Here are some red flags indicating that a website may be fake:" and "Protect yourself online by following these key security steps:".

## Taxonomy Design Observations

- Kept the taxonomy simple by including only the main intent `identify_fake_websites` per user instructions, discarding the secondary candidates.

## Edge Cases Noticed During Extraction

- The page discusses how links might display one destination but resolve to another (requiring hovering to inspect).

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded `identify_fake_websites`, `check_order_history`, and `report_suspicious_website`.
- The user approved `identify_fake_websites` and rejected the others to maintain a focused taxonomy.
- The final taxonomy is documented in taxonomy.md.
