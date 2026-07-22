# Notes

## General Observations About the Page

The page outlines the card brand qualifications, digital product restrictions, shipping window constraints, and exception handling for declined payments when using the Amazon Currency Converter.

---

## Navigation Structure

This is a short, single-topic help article with a flat list structure.

---

## Page Quality Observations

Clear and concise, with a dedicated warning note on handling declined payments to maintain the converter currency selection.

---

## Missing Documentation

Does not detail the list of all supported currencies (redirects to the Supported Currencies page) or list specific decline error codes.

---

## Missing Intents (Intentionally Excluded)

- Excluded general card setup in Wallet or general order payment decline troubleshooting (these are covered by separate dedicated pages: `manage_payment_details` and `resolve_declined_payment`).

---

## Retrieval Challenges

Direct queries about card brands or shipping windows for currency converter must map to this general requirements intent.

---

## RAG Chunking Recommendations

Since it's a short, single-topic page, the entire article should be treated as a single chunk.

---

## Intent Ambiguity Observations

Potential minor overlap with general payment decline resolution, but here it is specific to maintaining the currency converter.

---

## Reusable Extraction Patterns

- "To qualify to use..."
- "To resolve a declined payment on... you must..."

---

## Taxonomy Design Observations

Grouped the declined payment exception under the parent requirements check category `check_currency_converter_requirements` to maintain a simple, hierarchical structure.

---

## Edge Cases Noticed During Extraction

- Kindle eBooks are the only digital product/subscription allowed.
- Estimated shipping window is local currency dependent (14 vs 30 days).
- Changing to an ineligible payment method during payment declines will result in losing the converter.

---

## Iteration 1 - Observations (2026-07-22)

- **Important extraction observations**: Identified specific card brand rules and order-level restrictions (digital, shipping window).
- **Approved taxonomy changes**: Approved ADD for parent `check_currency_converter_requirements` and MERGE for sub-intent `resolve_declined_currency_converter_payment`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: General card brand queries resolve to the parent; declined converter payments resolve to the sub-intent.
- **Taxonomy decisions**: Maintained parent-child relationship to avoid bloating top-level payment methods.
- **Chunking observations**: Ideal for single-chunk retrieval.
- **Notable edge cases**: Kindle eBook exception and shipping window difference by currency.
- **Lessons useful for future pages**: Map exception paths (declined payment rules) as sub-intents under the main feature rules page.
