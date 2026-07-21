# Notes

## General Observations About the Page

The page explains the purpose of Amazon's online consumer surveys, including how invitations are issued, the potential for gift card incentives, security guidelines to identify authentic surveys, and scam reporting procedures.

---

## Navigation Structure

The page content is organized sequentially:
1. Overview of online surveys and third-party hosting.
2. Gift card reward details and delivery timeframe.
3. Security warning about sensitive information and instructions for reporting scams.
4. Privacy Notice applicability statement.

---

## Page Quality Observations

The page is highly readable, concise, and provides clear, actionable instructions on how to identify fake surveys and report scam emails.

---

## Missing Documentation

The page does not specify the exact names of the third-party survey hosts that Amazon uses, nor does it detail the specific criteria for receiving an invitation.

---

## Missing Intents (Intentionally Excluded)

- `receive_survey_reward`: Proposing a standalone intent for claiming or receiving the survey reward was rejected because reward delivery is an integrated benefit of completing the survey rather than an independent user task.

---

## Retrieval Challenges

Users searching for "Amazon survey gift card" or "did not receive survey reward" must map to `take_consumer_survey`, as no separate reward intent was approved.

---

## RAG Chunking Recommendations

We recommend dividing the page into two main chunks:
1. Survey Participation & Rewards: Covers survey invitations, third-party hosting, and gift card rewards.
2. Survey Security & Scam Reporting: Covers what Amazon surveys never ask for and how to report phishing survey emails.

---

## Intent Ambiguity Observations

There is potential overlap with general scam-reporting pages, but this page specifically focuses on survey-themed phishing attempts.

---

## Reusable Extraction Patterns

- "We occasionally invite you to take online surveys..."
- "Amazon.com surveys never ask you to provide..."
- "If you receive an Amazon.com email... notify us immediately at..."

---

## Taxonomy Design Observations

The taxonomy has been simplified by rejecting a separate reward-related intent, focusing instead on the core user activities of participating in legitimate surveys and reporting suspicious ones.

---

## Edge Cases Noticed During Extraction

- Third-party sites hosting official Amazon surveys.
- Two-week delay for receiving gift card rewards.
- Receiving an email invite requesting passwords or social security numbers.

---

## Iteration 1 - Observations (2026-07-21)

- **Important extraction observations**: Focused on survey invitations, reward delivery terms, and recognizing/reporting survey phishing scams.
- **Approved taxonomy changes**: Added the intents `take_consumer_survey` and `report_survey_scam`.
- **Rejected taxonomy changes**: Proposing `receive_survey_reward` was rejected.
- **Retrieval observations**: Queries regarding survey validity and rewards will map to this page.
- **Taxonomy decisions**: Maintained two distinct intents: one for taking surveys and one for security/reporting scams, avoiding unnecessary intent proliferation.
- **Chunking observations**: Coherent division between participation details and security safeguards.
- **Notable edge cases**: The two-week delivery window for gift card incentives and third-party survey hosts.
- **Lessons useful for future pages**: Differentiate transactional incentives from primary tasks, and isolate safety/security actions as distinct intents.
