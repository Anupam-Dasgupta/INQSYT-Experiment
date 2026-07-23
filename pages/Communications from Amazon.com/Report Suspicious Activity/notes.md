# Notes

## General Observations About the Page

- The page outlines how to report various suspicious activities on Amazon, including suspicious products/sellers, suspected stolen property, and communication scams.

## Navigation Structure

- Direct instructions for reporting.
- Links to related workflows: Product page report flows, Report a Scam page link, California Office of the Attorney General link.

## Page Quality Observations

- Document is brief but provides actionable links.
- Clearly distinguishes between general product/seller issues, stolen property, and scams.

## Missing Documentation

- Step-by-step UI directions for customer service reporting flows could be more detailed.

## Missing Intents (Intentionally Excluded)

- `report_amazon_scam`: Merged and renamed to `report_scam_call_message` under `report_suspicious_activity` super-intent.

## Retrieval Challenges

- The term "suspicious activity" is broad and overlaps with scam/fraud identification.

## RAG Chunking Recommendations

- Chunk 1: Product page reporting steps and CS chat/phone options.
- Chunk 2: Suspected stolen goods reporting and California Attorney General details.

## Intent Ambiguity Observations

- Overlap between reporting product issues and general seller feedback.

## Reusable Extraction Patterns

- Cues like "Submit a report on...", "If you suspect...", and "Follow the instructions in...".

## Taxonomy Design Observations

- Configured `report_suspicious_activity` as a super-intent with sub-intents: `report_suspicious_product_or_seller`, `report_stolen_property`, and `report_scam_call_message` to satisfy specific user requirements.

## Edge Cases Noticed During Extraction

- Special reporting flow/link provided specifically for California residents reporting stolen goods.

## Iteration 1 - Observations (2026-07-23)

- Initial candidate extraction yielded `report_suspicious_product_or_seller`, `report_stolen_property`, and `report_amazon_scam`.
- The user instructed to create a super-intent `report_suspicious_activity` with the candidates and `report_scam_call_message` as sub-intents.
- The final taxonomy is documented in taxonomy.md.
