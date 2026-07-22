# Notes

## General Observations About the Page

The page helps customers identify and troubleshoot unrecognized or unknown charges from Amazon on their card/bank statements. It lists common sources of unrecognized charges (e.g. Amazon Prime, digital subscriptions, split orders, bank authorizations, or family purchases) and provides a list of statement descriptors commonly used by Amazon (e.g. `AMZN.COM/BILL`, `Amazon Digital Svcs`).

---

## Navigation Structure

The page is organized as follows:
1. Header: "Unknown Amazon Payment Charges"
2. Introductory list of common reasons for unrecognized charges.
3. Troubleshooting section with subheadings for specific charges (Amazon Prime, digital subscriptions, authorizations, split shipments, etc.).
4. A list of statement descriptors with descriptions of what they represent.
5. Action steps to match the charge against transaction history using "Your Transactions".

---

## Page Quality Observations

The page is highly useful as it links bank statement descriptors directly to the corresponding Amazon service, which is a major pain point for users. It also clearly explains how split shipments and pending authorizations appear as separate charges.

---

## Missing Documentation

The page does not explain how to proceed if the descriptor seen on the statement is not in the provided table, or how to contact customer service directly to resolve an unrecognized charge.

---

## Missing Intents (Intentionally Excluded)

- Excluded general billing dispute forms or bank chargeback claim procedures (these are external bank processes).

---

## Retrieval Challenges

Queries like "why was I charged $14.99", "descriptor AMZN.COM/BILL", "unauthorized charge", or "double charged" must map back to this page. Incorporating the exact descriptors into search terms is helpful.

---

## RAG Chunking Recommendations

We recommend splitting the document into three distinct chunks:
1. Common Reasons & Troubleshooting: Covers Prime memberships, digital subscriptions, split shipping, and family purchases.
2. Statement Descriptors Table: Keeps the table of descriptors as a single chunk to preserve the mapping context.
3. Verification & Recovery Actions: Covers navigating to "Your Transactions" to match prices.

---

## Intent Ambiguity Observations

There could be overlap with general payment issues, but this page is uniquely focused on identifying post-transaction unrecognized charges.

---

## Reusable Extraction Patterns

- "An unknown Amazon charge is probably..."
- "For help identifying the unknown charge, refer to..."
- "Check your statement for..."

---

## Taxonomy Design Observations

Consolidated all unrecognized charge troubleshooting, descriptor lists, and transaction verification steps under the single intent `identify_unknown_charge` to maintain a streamlined taxonomy.

---

## Edge Cases Noticed During Extraction

- A pending authorization is not an actual charge and will disappear according to bank policy.
- Split shipments result in separate charges that sum up to the order total.
- Family members or coworkers using the same card can trigger unexpected charges.

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Mapped specific bank statement descriptors to corresponding Amazon services.
- **Approved taxonomy changes**: Added the intent `identify_unknown_charge`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: Highly likely that queries containing raw descriptor strings (e.g. "AMZN Digital") will search for this intent.
- **Taxonomy decisions**: Grouping diagnosis (descriptors) and solution (Your Transactions check) under one intent prevents fragmented categories.
- **Chunking observations**: Tabular data mapping descriptors to services is best kept contiguous.
- **Notable edge cases**: Split shipments creating multiple smaller statement lines.
- **Lessons useful for future pages**: Troubleshooting pages explaining charge descriptors are highly informational and action-oriented.

## Iteration 2 - Observations (2026-07-22)

- **Important extraction observations**: Re-confirmed that matching unrecognized bank statement line-items to Amazon transaction history remains consolidated under a single troubleshooting intent.
- **Approved taxonomy changes**: Confirmed the ADD proposal for `identify_unknown_charge` and updated the taxonomy to the 5-column schema with empty sub-intent cells for uniformity.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: Highly likely that user searches for descriptor strings like "AMZN.COM/BILL" or "AMZN Digital" will route here.
- **Taxonomy decisions**: Keeping a single broad intent captures both statement line-item identification and verification steps.
- **Chunking observations**: Keeping the list of statement descriptors as a standalone chunk remains key to retaining complete context.
- **Notable edge cases**: Split orders appearing as separate statement lines and temporary bank authorizations.
- **Lessons useful for future pages**: Ensure all flat-taxonomy single-intent pages consistently adopt the 5-column sub-intent layout with empty cells for standardized integration.
