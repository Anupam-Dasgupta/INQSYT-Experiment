# Curation

## Initial Page Observations
The page provides direct tracking steps, defines various delivery statuses, explains some troubleshooting (delayed, unshipped), and links out to carriers or missing package pages.

## Page Understanding
The primary goal is order tracking. A secondary goal is troubleshooting delivery expectations.

## Intent Extraction Notes
Extracted intents supported natively on the page. Ignored intents where the only action is navigating to another page (except where initially captured as candidates for review).

## Supporting Evidence Collected for Each Intent
- **`track_package`**: "To get tracking numbers and delivery updates... Go to Your Orders - Find the order you want to track - Select track package next to your order"
- **`track_third_party_package`**: "You can only view tracking information if: - the third-party seller shares this info with us - you chose a trackable shipping option"
- **`understand_delivery_statuses`**: "Your delivery status is in Your Orders: - Arriving: usually followed by a date... - Out for delivery: ... - Delivered: ... - Undeliverable: ..."
- **`solve_delivery_problems`**: "Solving delivery problems You can check what to do when: - Order hasn't shipped yet: ... - Order is delayed: ... - Missing package: ... - Missing items: ..."
- **`contact_carrier`**: "To contact the company that's delivering your package, go to contact a carrier."

## Intent Boundary Discussions
There was ambiguity on whether to include "missing items" and "missing packages" under `solve_delivery_problems` since the page only provides redirect links for them, rather than solving the problem natively on the page itself.

## Candidate Merge Opportunities
- MERGE `track_third_party_package` into `track_package` because the action (tracking) is identical.

## Candidate Split Opportunities
- SPLIT `solve_delivery_problems` into `understand_unshipped_order` and `understand_delayed_order` (removing missing item/package as they redirect).

## Candidate Rename Discussions
- RENAME `understand_delivery_statuses` to `check_delivery_status_meaning` to have clearer action-oriented verbs.

## Deleted Candidate Intents and the Reasons
- DELETE `contact_carrier`. Reason: The page only provides a link to an outside page for contacting a carrier.

## Added Candidate Intents and the Reasons
- None

## Taxonomy Change Proposals
1. SPLIT `solve_delivery_problems` into `understand_unshipped_order` and `understand_delayed_order`.
2. DELETE `contact_carrier`.
3. MERGE `track_third_party_package` into `track_package`.
4. RENAME `understand_delivery_statuses` to `check_delivery_status_meaning`.

## Human Approvals and Rejections
- Proposal 1 (SPLIT): Rejected by human reviewer.
- Proposal 2 (DELETE): Approved by human reviewer.
- Proposal 3 (MERGE): Approved by human reviewer.
- Proposal 4 (RENAME): Approved by human reviewer.

## Final Curation Decisions
Applied the approved Merge, Delete, and Rename proposals. Retained `solve_delivery_problems` as it was originally extracted since the split proposal was rejected.

## Validation Notes
- Verified all format constraints and schema matches.
- Verified evidence grounds the intents properly.
- All 4 step checks were explicitly approved by the human reviewer.

## Assumptions Made During Extraction
- Assumed third-party package tracking is just a variant of standard tracking due to the shared UI location ("Your Orders").
