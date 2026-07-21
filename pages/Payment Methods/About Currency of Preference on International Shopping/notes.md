# Notes

## General Observations About the Page

The page describes the "Currency of Preference on International Shopping" feature on Amazon. It explains that this display-only feature allows international customers to view prices and order totals in one of over 80 supported currencies. It also highlights the distinction between the display-only "Currency of Preference" and the "Amazon Currency Converter" which handles the actual payment/charging currency.

---

## Navigation Structure

The page is organized into the following sections:
1. Header: "About Currency of Preference on International Shopping"
2. Opening explanation of the Currency of Preference display-only feature and default setting (USD).
3. Explanation of the checkout experience (Order Total in preferred currency, Payment Total in charged currency).
4. Outline of eligibility for actual card charging via the Amazon Currency Converter.
5. List of available currencies for international shopping.

---

## Page Quality Observations

The distinction between browsing currency (display-only) and payment currency (charged to the card) is critical and clearly explained. The table of available currencies provides complete visibility for international shoppers.

---

## Missing Documentation

The page does not explain how regional currency detection affects default settings if a user does not explicitly choose a preferred currency.

---

## Missing Intents (Intentionally Excluded)

None. The single intent `change_currency_of_preference` covers all topics on this page.

---

## Retrieval Challenges

Customers searching for "how to change language/currency settings", "why are prices in USD", or "supported shopping currencies" must map back to this page. Syntactic mappings for terms like "Currency of Preference" are helpful.

---

## RAG Chunking Recommendations

We recommend chunking the page into two parts:
1. Feature Description and Checkout: Covers how the display-only feature works and the checkout details.
2. Supported Currencies List: Covers the list of available currencies for international shopping.

---

## Intent Ambiguity Observations

There is minor overlap with "Amazon Currency Converter Requirements" or "Select Your Card Currency". However, this page is uniquely about the *display-only* browsing currency of preference, whereas the converter pages cover checkout card billing currency.

---

## Reusable Extraction Patterns

- "Currency of Preference is a display-only feature and allows you to see..."
- "You can update your Currency of Preference by changing from..."
- "At checkout, an 'Order Total' will display..."

---

## Taxonomy Design Observations

Consolidated the display-only setting and the list of supported browsing currencies under the single intent `change_currency_of_preference` to prevent taxonomy bloat.

---

## Edge Cases Noticed During Extraction

- Currency of Preference is a display-only feature; it does not change the currency charged to the card unless used in conjunction with the Currency Converter.
- Available only for international shopping (not domestic US shoppers).

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Extracted display currency settings and the distinction between browsing and payment currency.
- **Approved taxonomy changes**: Added the intent `change_currency_of_preference`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: High likelihood of queries targeting "prices in local currency" or "shop in my currency" mapping to this intent.
- **Taxonomy decisions**: Grouped the browsing currency features under a single settings-focused intent.
- **Chunking observations**: Separating the functional details of the feature from the long list of supported currencies is useful for precise retrieval.
- **Notable edge cases**: The separation between display/order total (browsing currency) and payment total (charging currency).
- **Lessons useful for future pages**: Differentiating browsing display settings from transactional payment settings is key to correct intent routing.
