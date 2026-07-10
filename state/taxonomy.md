# Taxonomy

**Source Page URL:** `https://www.amazon.com/gp/help/customer/display.html?nodeId=GENAFPTNLHV7ZACW`
**Page Title:** Tracking your package - Amazon Customer Service
**Short Page Summary:** This page helps customers track their orders and understand the current delivery status of their packages, including those from third-party sellers, and provides initial troubleshooting for delayed or unshipped orders.

## Intent Hierarchy
Flat

## Extracted Candidate Intents
- `track_package`
- `track_third_party_package`
- `understand_delivery_statuses`
- `solve_delivery_problems`
- `contact_carrier`

## Final Approved Intent List
- `track_package`
- `check_delivery_status_meaning`
- `solve_delivery_problems`

## Parent-Child Relationships
N/A

## Synonyms or Alternate Phrasings Observed
- "find tracking numbers"
- "delivery updates"
- "view tracking information"

## Duplicate or Overlapping Intents
- `track_third_party_package` overlapped with `track_package` as both require the customer to navigate to "Your Orders" for tracking updates.

## Intent Naming Rationale
- `understand_delivery_statuses` was renamed to `check_delivery_status_meaning` to align better with a strictly concise `verb_object` format indicating a clearer action.

## Final Taxonomy
After all approved change proposals have been applied:
- **`track_package`**: Track a package or get delivery updates for an order, including packages sold by a third-party seller.
- **`check_delivery_status_meaning`**: Understand the meaning of different delivery statuses like Arriving, Delivered, etc.
- **`solve_delivery_problems`**: Figure out what to do if an order is delayed, hasn't shipped, or is missing.
