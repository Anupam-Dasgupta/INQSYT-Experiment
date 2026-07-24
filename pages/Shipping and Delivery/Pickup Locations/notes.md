# Notes

## General Observations About the Page

- The page introduces Amazon's self-service and counter-service pickup options (Amazon Locker, Counter, UPS Access Points) as alternatives to home delivery.

## Navigation Structure

- Short explanation paragraph, direct links to search.
- Links to: Amazon pickup search portal.

## Page Quality Observations

- Very concise, focusing on letting customers know that delivery options are shown during checkout.

## Missing Documentation

- Step-by-step pick-up rules (e.g., how many days to retrieve packages, how to open lockers).

## Missing Intents (Intentionally Excluded)

- `search_pickup_locations` was rejected in favor of the custom `check_opening_hours` sub-intent and the renamed `select_pickup_location` super-intent.

## Retrieval Challenges

- The help document is brief, missing granular operational details like locker retrieval codes or size/weight constraints.

## RAG Chunking Recommendations

- Single Chunk: Entire pickup options overview and search link.

## Intent Ambiguity Observations

- Overlap with standard address selections during checkout.

## Reusable Extraction Patterns

- Terms like "Instead of having a package delivered...", "Amazon Locker, Amazon Counter, or UPS AccessPoints™".

## Taxonomy Design Observations

- Renamed main super-intent to `select_pickup_location` and added the user-requested sub-intent `check_opening_hours`.

## Edge Cases Noticed During Extraction

- Availability is determined dynamically during checkout based on eligibility and item size.

## Iteration 1 - Observations (2026-07-24)

- Initial extraction of candidates.
- The user requested renaming the super-intent to `select_pickup_location` and adding `check_opening_hours` as a sub-intent while discarding the search sub-intent.
- The final taxonomy is documented in taxonomy.md.
