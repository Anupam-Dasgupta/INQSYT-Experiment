# Notes

## General Observations About the Page

The page describes how a customer can select or update their card currency for the Amazon Currency Converter at checkout. It provides separate, step-by-step instructions for desktop and mobile devices.

---

## Navigation Structure

The page is organized into the following sections:
1. Header: "Select Your Card Currency for Amazon Currency Converter"
2. Opening paragraph detailing eligibility and region-based automatic detection.
3. Steps for Desktop checkout.
4. Steps for Mobile checkout.
5. Clarification notes (payment total displayed in card currency, Amazon stores card currency settings).
6. Troubleshooting guidance if the option is not visible.

---

## Page Quality Observations

The step-by-step instructions for both desktop and mobile are clear and align well with actual UI checkout flows. Highlighting that settings are stored for future purchases is helpful for user expectation.

---

## Missing Documentation

The page does not explain how to handle cards that support multiple currencies or how Amazon handles default billing currencies if the regional detection fails.

---

## Missing Intents (Intentionally Excluded)

None. The single intent `select_card_currency_for_currency_converter` fully covers the checkout procedures described on this page.

---

## Retrieval Challenges

User queries like "why can't I pay in my local currency?", "change checkout currency", or "mobile currency settings" must map back to this page. Clear synonyms for "update" and "change" should be handled.

---

## RAG Chunking Recommendations

We recommend chunking the page into two parts:
1. Overview & Desktop Steps: Covers eligibility and desktop checkout instructions.
2. Mobile Steps & Troubleshooting: Covers mobile checkout instructions and troubleshooting instructions if the option is missing.

---

## Intent Ambiguity Observations

There is mild overlap with checking supported currencies or requirements. However, this page is specifically focused on the user action of *selecting* or *changing* the currency during checkout.

---

## Reusable Extraction Patterns

- "If your order is eligible for..., the option to pay in... will be displayed..."
- "If you want to change your..., you can update it at the checkout:"
- "To change your card currency: 1. Go to... 2. Select..."

---

## Taxonomy Design Observations

Consolidated both mobile and desktop update procedures under the single intent `select_card_currency_for_currency_converter` to maintain a concise taxonomy.

---

## Edge Cases Noticed During Extraction

- Regional regional-based detection is used to automatically determine card currency.
- Option is hidden if the order or payment method is ineligible.
- Saved settings automatically apply to future eligible purchases.

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Extracted step-by-step procedures for desktop and mobile checkout flows.
- **Approved taxonomy changes**: Added the intent `select_card_currency_for_currency_converter`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: Users searching for "how to change currency on phone/mobile" or "pay in usd instead of inr" should retrieve this page.
- **Taxonomy decisions**: Keeping desktop and mobile procedures unified under one intent avoids duplicate taxonomy entries for the same customer goal.
- **Chunking observations**: Splitting by platform (desktop vs mobile) helps keep RAG search precise depending on the user's interface.
- **Notable edge cases**: Storing card currency preferences for future checkouts.
- **Lessons useful for future pages**: Action-oriented support pages with dual desktop/mobile paths are best represented as a single intent.
