# Notes

## General Observations About the Page

- The page covers techniques for customers to identify fake/phishing phone calls claiming to be from Amazon.
- Explains key indicators of fraudulent calls, including caller requests for payment, remote access, passwords/OTPs, or creating false subscription/order emergencies.

## Navigation Structure

- High-level list of tips for phone calls verification.
- Links to related help topics: Identifying a scam, How to identify fake emails, How to identify fake text messages/SMS, How to identify fake websites, Report a scam.

## Page Quality Observations

- The document is clear and readable.
- Direct links are provided for verification.
- Includes advice on order history verification.

## Missing Documentation

- No clear visual or audio example of typical call scams (like typical robo-call scripts).

## Missing Intents (Intentionally Excluded)

- `check_order_history`: Excluded because checking order history is a verification action performed on the order history page, not a direct capability of this page.
- `report_suspicious_call` / `report_amazon_scam`: Excluded because reporting scams is a distinct user goal supported by the dedicated "Report a scam" page.

## Retrieval Challenges

- High conceptual overlap with other fraud pages (emails, websites, SMS) due to similar indicators.

## RAG Chunking Recommendations

- Chunk 1: Suspicious caller behaviors (payments, remote access, passwords).
- Chunk 2: Emergency claims (subscriptions expiring, unauthorized purchases) and actions to take.

## Intent Ambiguity Observations

- Ambiguity may occur between general scam verification and phone-call-specific verification.

## Reusable Extraction Patterns

- Cues like "If you receive a suspicious phone call from someone claiming to be from Amazon, be alert if they:" and "Amazon will never ask you...".

## Taxonomy Design Observations

- Kept the taxonomy simple by including only the main intent `identify_fake_phone_calls` per user instructions, discarding the secondary candidates.

## Edge Cases Noticed During Extraction

- The page highlights remote access requests (e.g. AnyDesk, TeamViewer) as a key indicator of call fraud.

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded `identify_fake_phone_calls`, `check_order_history`, and `report_suspicious_call`.
- The user approved `identify_fake_phone_calls` and rejected the others to maintain a focused taxonomy.
- The final taxonomy is documented in taxonomy.md.
