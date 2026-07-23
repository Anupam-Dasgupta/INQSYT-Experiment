# Notes

## General Observations About the Page

- The page reviews common scam trends observed by Amazon (order confirmations, tech support, membership renewal, account suspension/deletion, fake recalls/refunds, and recruitment scams).

## Navigation Structure

- High-level summaries of current scam trends.
- Links to related help topics: Identifying a scam, How to identify fake emails/SMS/phone calls/websites, Report a scam, Better Business Bureau Scam Tracker.

## Page Quality Observations

- Highly structured and clear.
- Provides actionable steps (e.g. check order history, use Scam Tracker).

## Missing Documentation

- Real-world screenshots of actual phishing templates/messages would be useful.

## Missing Intents (Intentionally Excluded)

- `verify_order_history`: Excluded because verification is done on the order history page.
- `report_amazon_scam`: Excluded because scam reporting is done on the dedicated "Report a scam" page.

## Retrieval Challenges

- The document covers multiple highly distinct scam topics in a single page.

## RAG Chunking Recommendations

- Chunk 1-6: Separate chunks for each scam type (Order confirmation, Tech support, Prime membership, Account suspension, Recall/refund, Recruitment scams).
- Chunk 7: BBB Scam Tracker partnership details.

## Intent Ambiguity Observations

- High conceptual overlap between general scam identification and specific trend reviews.

## Reusable Extraction Patterns

- Cues like "Review a sample of common scam trends:" and sections detailing each type.

## Taxonomy Design Observations

- Standardized `check_scam_trends` as the super-intent, preserving the 6 specific scam types as sub-intents to capture full page granularity.

## Edge Cases Noticed During Extraction

- Inclusion of recruitment scams, which often target job-seekers outside the typical consumer purchasing flow.

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded the super-intent and the 6 sub-intents.
- The user approved this taxonomy configuration.
- The final taxonomy is documented in taxonomy.md.
