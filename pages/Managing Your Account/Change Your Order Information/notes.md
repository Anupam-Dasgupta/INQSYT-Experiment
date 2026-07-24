# Notes

## General Observations About the Page

This page provides comprehensive assistance for users wishing to change information (such as shipping address, billing address, payment method, and quantity) on orders that have not yet been dispatched.

---

## Navigation Structure

The page describes the main steps to change order details from the desktop interface:
- Navigate to Your Orders.
- Select Order Details and click "Change" next to the details to be updated.
It also highlights navigation and redirection rules for platform variations (mobile vs. desktop), third-party seller shipments, and Amazon Fresh/Whole Foods deliveries.

---

## Page Quality Observations

The guidance is structured and clear. It clearly warns mobile users about platform constraints (not being able to edit addresses on mobile devices). It also redirects users to appropriate pages/actions for third-party sellers and Fresh orders.

---

## Missing Documentation

The page does not specify:
- How long after an order is placed can it be modified (what defines "not yet been dispatched" in terms of timing or order status).
- What details *cannot* be changed (e.g., changing the product model or size).
- If changing the payment method will trigger re-authorization or affect delivery timelines.

---

## Missing Intents (Intentionally Excluded)

- `contact_third_party_seller`: Excluded as a standalone generic intent because contacting the seller is a fallback mechanism specifically for updating delivery addresses on their orders, which is fully represented under `update_third_party_order_address`.
- `modify_upcoming_delivery_settings`: Excluded as a generic intent since the Fresh delivery modification relates to the specific procedural action of adding items to the delivery.

---

## Retrieval Challenges

- Users might search for "change delivery address" or "update shipping location" without specifying whether the order is shipped by Amazon or a third-party seller, or whether they are on a mobile device. A RAG system must retrieve the platform restrictions and third-party fallback options alongside the standard desktop path to avoid confusion.

---

## RAG Chunking Recommendations

We recommend chunking this page into:
1. **Standard Desktop Order Update Procedure**: Steps to modify unshipped orders via desktop.
2. **Mobile Device Constraints**: Platform-specific limitations for updating payment details but not addresses.
3. **Third-Party Seller Order Updates**: Actions for updating delivery addresses on third-party orders.
4. **Amazon Fresh/Whole Foods/Merchant Delivery Updates**: Actions for adding items to upcoming grocery/fresh orders.

---

## Intent Ambiguity Observations

- Users may fail to distinguish between standard Amazon-shipped orders and third-party seller-shipped orders when trying to update shipping addresses.
- Grouping both under `change_order_information` helps guide users through the correct branch.

---

## Reusable Extraction Patterns

- Platform constraint patterns: "If you are on a [platform] device, you can [action], but not [action]."
- Fallback/redirect patterns: "To [action] of an order from [entity], go to [link/destination]."

---

## Taxonomy Design Observations

- Renamed candidate `change_order_information` to `change_order_details` to avoid name collision with the proposed super-intent `change_order_information`.
- Grouped all sub-intents (details change, mobile flow, third-party seller address, and Fresh delivery items) under the super-intent `change_order_information` for a clean hierarchy.

---

## Edge Cases Noticed During Extraction

- Mobile platform constraint: Address modifications are blocked on mobile devices, prompting users to visit the desktop site.
- Fresh delivery modification: Adding items is only supported for "upcoming" Fresh, Whole Foods, and merchant deliveries.

---

## Iteration 1 - Observations (2026-07-24)

- Extracted 4 candidate intents capturing standard updates, mobile constraints, third-party seller fallbacks, and grocery delivery modifications.
- Renamed standard update intent to `change_order_details` and successfully merged all 4 under the super-intent `change_order_information`.
