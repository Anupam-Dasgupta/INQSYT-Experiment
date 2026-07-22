# Notes

## General Observations About the Page

This page provides step-by-step instructions for managing shipping addresses on an Amazon customer account. It covers the primary operations of adding, editing, deleting, and setting a default address, along with constraints like Subscribe & Save restrictions and payment confirmation requirements.

---

## Navigation Structure

The page is structured linearly with bold headers for each sub-procedure:
- Add a new address
- Edit an address
- Delete an address
- Set a default shipping address
It also includes a section at the bottom for redirecting users who want to change their address on open orders or wish lists.

---

## Page Quality Observations

The documentation is clear and easy to follow. Each section has a bold title followed by simple, imperative instructions. Readability is high, though it includes external redirects for open orders and wish lists, which are not self-contained on this page.

---

## Missing Documentation

The page does not specify:
- How to manage international shipping addresses or specific formatting rules.
- How to add delivery instructions (e.g., gate codes, safe drop locations) beyond a generic mention of "delivery preferences."

---

## Missing Intents (Intentionally Excluded)

- `change_shipping_address_on_open_orders`: Excluded because the task must be completed on a separate page ("Change Your Order Information").
- `change_shipping_address_on_wish_list`: Excluded because it redirects to the wish list page ("Create Your List").

---

## Retrieval Challenges

- The restriction on deleting addresses due to Subscribe and Save orders is a common user pain point. Storing this under a generic delete intent could make it harder to retrieve if a user searches specifically for "why can't I delete my address?"
- The requirement to verify the payment card when using a newly added address is a post-condition constraint that must be retrieved together with address creation/modification queries.

---

## RAG Chunking Recommendations

Recommend splitting the content into three distinct chunks:
1. **Add and Edit Address Procedure**: Covers adding new addresses, editing details, and the payment card verification warning.
2. **Delete Address and Set Default**: Covers deleting addresses (with the Subscribe & Save restriction) and setting an address as default (checkout implications).
3. **Open Orders and Wish List Redirects**: Focuses on redirection instructions for active orders and wish lists.

---

## Intent Ambiguity Observations

There is potential overlap between editing an address and managing delivery preferences. Treating them as sub-intents under the `manage_addresses` super-intent helps group them cleanly and resolves boundary issues.

---

## Reusable Extraction Patterns

- Goal-oriented instruction start: "To [action], select [element]."
- Hard constraint structure: "You can't [action] with [condition]. First, [remediation]."
- Redirection pattern: "For [feature], visit [page]."

---

## Taxonomy Design Observations

Merged candidate intents `add_address`, `edit_address`, `delete_address`, and `set_default_address` under `manage_addresses` super-intent. This avoids having multiple tiny, fragmented intents and mirrors the account dashboard's structural layout.

---

## Edge Cases Noticed During Extraction

- Users cannot delete addresses that are linked to active Subscribe & Save orders. They must first update the subscription.
- Adding or editing an address triggers a verification request for the payment card number during the next checkout.

---

## Iteration 1 - Observations (2026-07-22)

- Extracted candidate intents (`add_address`, `edit_address`, `delete_address`, `set_default_address`).
- Approved merging all candidate intents under the `manage_addresses` super-intent.
- Documented navigation structure, page quality observations, and critical retrieval challenges (e.g., Subscribe & Save exceptions).
- Outlined three distinct semantic chunks for RAG.
