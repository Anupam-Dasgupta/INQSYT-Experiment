# Notes

## General Observations About the Page

- The page outlines terms and rules for Amazon's guaranteed delivery offerings, including eligible delivery speeds, costs, and refund conditions if delivery is late.

## Navigation Structure

- Direct list of terms, criteria, and FAQ elements.
- Links to: Recommended topics on placing guaranteed delivery orders.

## Page Quality Observations

- Clearly defines the refund mechanism (automatic refund of shipping fees if a guaranteed attempt is late).

## Missing Documentation

- Step-by-step procedure on how to submit a customer support claim if the refund is not automatically processed.

## Missing Intents (Intentionally Excluded)

- None.

## Retrieval Challenges

- High possibility of users searching for general delivery delays rather than guaranteed delivery policy delays.

## RAG Chunking Recommendations

- Chunk 1: Guaranteed delivery eligibility & speed/cost messaging at checkout.
- Chunk 2: Late attempt shipping fee refund criteria.
- Chunk 3: Order countdown timer rules & timezone factors.

## Intent Ambiguity Observations

- Potential overlap between checking package tracking/status vs. checking delivery guarantees.

## Reusable Extraction Patterns

- Patterns like "We offer guaranteed delivery...", "If we provide a guaranteed delivery date and a delivery attempt isn't made...", "order within countdown timer".

## Taxonomy Design Observations

- Established `check_delivery_guarantees` as the super-intent, with `claim_late_delivery_refund` and `check_order_countdown_timer` as sub-intents.

## Edge Cases Noticed During Extraction

- Missed attempts (e.g., if the courier attempts delivery but cannot access the building) are counted as an attempt and thus do not qualify for the refund.

## Iteration 1 - Observations (2026-07-24)

- Initial extraction of candidates.
- The user approved the recommended configuration mapping the super-intent to the two sub-intents.
- The final taxonomy is documented in taxonomy.md.
