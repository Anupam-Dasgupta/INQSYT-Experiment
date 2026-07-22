# Notes

## General Observations About the Page

The page lists all the currencies supported by the Amazon Currency Converter. It details the card brand eligibility (American Express, MasterCard, and Visa) for each currency, and the estimated shipping window associated with orders using that currency.

---

## Navigation Structure

The page has a flat hierarchical structure:
1. Header: "Amazon Currency Converter Supported Currencies"
2. Introductory sentence outlining card brand eligibility (Visa, MasterCard, American Express).
3. A large, structured table listing currencies, eligibility by card brand, and the estimated shipping window (typically 14 or 30 days).

---

## Page Quality Observations

The documentation is highly structured and clear. Presenting the currency compatibility in a table is effective. However, the estimated shipping window column lacks detailed explanation on why certain currencies have longer windows (e.g., 30 days) versus others (14 days).

---

## Missing Documentation

The page does not explain what happens if a credit card is issued by a bank that does not support DCC (Dynamic Currency Conversion) or what additional fees might be charged by the card issuer.

---

## Missing Intents (Intentionally Excluded)

- Excluded general card setup in Wallet or general order payment decline troubleshooting (these are covered by separate dedicated pages: `manage_payment_details` and `resolve_declined_payment`).

---

## Retrieval Challenges

Users might search for support for specific country currencies (e.g., "Can I pay in Euros?", "Do you support Indian Rupees?"). The retrieval system needs to successfully map specific currency names or codes to this page and this intent.

---

## RAG Chunking Recommendations

Since the page primarily consists of a long table of currencies, it should be chunked logically. A single chunk containing the introduction and the table is ideal if token limits permit. Given the tabular format, keeping the table whole or in large blocks preserves the row context.

---

## Intent Ambiguity Observations

There is low ambiguity since the page is specifically focused on currency support. Some users asking about "exchange rates" or "currency converter fees" might land here, but those are covered by other pages (like Exchange Rates).

---

## Reusable Extraction Patterns

- "Amazon Currency Converter is available when you use..."
- "The Amazon Currency Converter supports these currencies:"

---

## Taxonomy Design Observations

Consolidated currency support, card brand compatibility, and shipping windows under the single intent `check_currency_converter_supported_currencies` to avoid creating narrow, redundant intents.

---

## Edge Cases Noticed During Extraction

- Certain currencies like Brazilian Real (BRL), Boliviano (BOB), and Chilean Peso (CLP) do not support American Express.
- Shipping windows vary between 14 days and 30 days depending on the currency.

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Extracted card eligibility and currency mappings from the main support table.
- **Approved taxonomy changes**: Added the intent `check_currency_converter_supported_currencies`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: High likelihood of queries targeting specific currency names/codes (e.g., USD, EUR, INR) mapping here.
- **Taxonomy decisions**: Keeping the taxonomy concise by grouping currency list and card brand eligibility under one intent.
- **Chunking observations**: Tabular data is best kept contiguous to preserve relational context.
- **Notable edge cases**: American Express exclusions for certain South American currencies.
- **Lessons useful for future pages**: Tables containing large numbers of rows are best handled as a single semantic retrieval unit if possible.

## Iteration 2 - Observations (2026-07-22)

- **Important extraction observations**: Re-evaluated the page content and confirmed that it remains a lookup reference listing supported currencies and card brands.
- **Approved taxonomy changes**: Confirmed the ADD proposal for `check_currency_converter_supported_currencies` and updated the taxonomy to the 5-column schema with empty sub-intent cells for schema uniformity.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: User queries containing specific currency codes (USD, EUR, INR) or country names (India, Brazil, etc.) will resolve to this single intent.
- **Taxonomy decisions**: Keeping a single flat intent as it fully represents the page's narrow, list-based goal.
- **Chunking observations**: Since this is a lookup table, it is best kept as a single chunk to prevent losing tabular correlation.
- **Notable edge cases**: American Express exclusions for BRL, BOB, and CLP, which need to be kept intact inside the chunk.
- **Lessons useful for future pages**: Ensure pages with no sub-intents conform to the 5-column sub-intent schema layout with empty cells to keep the corpus taxonomy structures fully consistent.
