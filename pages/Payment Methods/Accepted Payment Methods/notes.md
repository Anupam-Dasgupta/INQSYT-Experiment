# Notes

## General Observations About the Page

The page covers the list of accepted payment instruments (credit cards, debit cards, prepaid cards, and government benefits like SNAP EBT and FSA/HSA) on Amazon.com. It is primarily a reference page, providing a list of accepted networks and payment methods, along with specific billing address or eligibility requirements.

---

## Navigation Structure

The page has a flat hierarchical structure:
1. Header: "Accepted Payment Methods"
2. General list of accepted cards/networks (Visa, MasterCard, Store Card, etc.)
3. Paragraph on Wallet access ("without having to place an order, in your Amazon Wallet")
4. Note on Gift Cards and split payments
5. Note on FSA/HSA cards and eligibility
6. Note on SNAP EBT cards and participating states

---

## Page Quality Observations

The documentation is clear and concise. However, critical restrictions (such as FSA/HSA billing address requirements and SNAP EBT participating states) are placed under a general "Note:" section rather than structured fields, which could easily be overlooked by readers or simplistic parsers.

---

## Missing Documentation

The page does not list which specific states participate in SNAP EBT on Amazon, instead referring the user to an external link (www.amazon.com/SNAP).

---

## Missing Intents (Intentionally Excluded)

- `manage_payment_details`: Excluded because wallet management represents a procedural task, whereas this page is primarily viewed by users checking acceptance rules.
- `pay_with_gift_card`: Excluded to keep the taxonomy consolidated; gift card rules on this page are brief and better served under the main acceptance/viewing intent.
- `pay_with_fsa_hsa` & `pay_with_snap_ebt`: Excluded to avoid taxonomy bloat; these government benefit notes are treated as details under general accepted payment methods.

---

## Retrieval Challenges

Queries regarding specific payment networks (e.g., "Can I use STAR?", "Does Amazon take JCB?") or benefits ("Can I use food stamps?") must be mapped back to the single broad intent `check_accepted_payment_methods` despite the differing terminology.

---

## RAG Chunking Recommendations

We recommend splitting the document into three distinct semantic chunks:
1. General Card Acceptance: Bulleted list of accepted card brands/networks.
2. Wallet and Gift Cards: Paragraphs on Wallet editing, Gift Cards, and split payment rules.
3. Government Benefits: Paragraphs regarding FSA/HSA and SNAP EBT conditions and exclusions.

---

## Intent Ambiguity Observations

There is potential overlap between general checkout queries ("how do I buy things") and checking accepted payment methods. However, checking payment method acceptance is a distinct informational query.

---

## Reusable Extraction Patterns

- "Amazon.com accepts a variety of..."
- "The following payment methods are available for use:"
- "...cards are accepted as payment methods for..."

---

## Taxonomy Design Observations

Consolidated all payment instrument details (debit, credit, gift cards, FSA/HSA, and SNAP EBT) under a single broad intent `check_accepted_payment_methods`. This avoids a fragmented taxonomy of single-sentence intents.

---

## Edge Cases Noticed During Extraction

- FSA/HSA billing addresses must be in the U.S.
- EBT Cash benefits cannot be used (only SNAP EBT).
- Split payment is only allowed between one card and a gift card, not between multiple cards.

---

## Iteration 1 - Observations (2026-07-16)

- **Important extraction observations**: Candidate intents covered various sub-rules (HSA, EBT, Wallet, Gift Cards, Split Payments) which were then evaluated for taxonomy impact.
- **Approved taxonomy changes**: Added the single broad intent `check_accepted_payment_methods`.
- **Rejected taxonomy changes**: Rejected separate intents for `manage_payment_details`, `pay_with_gift_card`, `pay_with_fsa_hsa`, and `pay_with_snap_ebt`.
- **Retrieval observations**: Retrieval strategies must ensure specific benefit queries map to the broader acceptance intent.
- **Taxonomy decisions**: Keeping a high threshold for adding new intents helps keep the taxonomy clean and manageable.
- **Chunking observations**: Clean semantic boundaries exist between general payment networks, wallet/gift card guidelines, and specialized benefit cards.
- **Notable edge cases**: Split payment rules (only one card + gift card).
- **Lessons useful for future pages**: Consolidating single-sentence rules under a parent intent prevents taxonomy explosion.

---

## Iteration 2 - Observations (2026-07-21)

- **Important extraction observations**: Re-evaluated candidates under the latest skill sets to represent sub-tasks (Wallet, Gift Cards, FSA/HSA, SNAP EBT) using merge-preserved sub-intents.
- **Approved taxonomy changes**: Approved MERGE of all 4 sub-intents under the super-intent `check_accepted_payment_methods`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: Users searching for specific cards (SNAP, HSA/FSA, Gift Cards) will match specific sub-intents under the main accepted payment methods category.
- **Taxonomy decisions**: Utilized MERGE semantics to represent specific candidate intents as sub-intents in a 5-column layout rather than rejecting them.
- **Chunking observations**: Chunks map cleanly to the individual sub-intents.
- **Notable edge cases**: HSA/FSA billing address limitations and EBT Cash exclusion.
- **Lessons useful for future pages**: Merging specific procedures as sub-intents of a broad informational parent preserves granular details while keeping the parent taxonomy clean.
