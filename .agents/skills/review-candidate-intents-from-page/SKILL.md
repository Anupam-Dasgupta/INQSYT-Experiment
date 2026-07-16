---
name: review-candidate-intents-from-page
description: Review page-level intent candidates and propose high-quality taxonomy refinements.
---

# Purpose

Review the extracted candidate intents for a page and determine whether the existing taxonomy should be refined.

This skill **never edits the taxonomy directly**.
It only proposes changes for human review.

The objective is **a compact, reusable, and scalable intent taxonomy**, not the most granular one.

---

# Inputs

- Source page URL
- PAGE_INTENT_CANDIDATES

---

# Required References

Read:

- specification/step1-schema.md

---

# Core Principle

The taxonomy should represent **user goals**, not individual sentences or isolated features.

A single sentence mentioning a capability **does not justify creating a new intent**.

Prefer fewer, broader intents whenever they naturally represent the same user goal.

---

# Decision Order

For every candidate intent, evaluate in the following order.

## 1. Can an existing intent already represent this?

If yes:

- Do NOT propose ADD.
- Recommend mapping it to the existing intent.
- Even if wording differs, prefer semantic similarity over exact wording.

Examples:

Existing:
- manage_notifications

Page mentions:
- promotional emails
- restock emails
- newsletters
- notification preferences

Do NOT propose four new intents.

They are all evidence supporting:

manage_notifications

---

## 2. Would expanding an existing intent make it sufficient?

If yes:

Propose:

- MERGE
or
- RENAME

instead of ADD.

Example:

Existing:

manage_cards

Page introduces:

- debit cards
- credit cards
- prepaid cards

Better proposal:

Rename

manage_cards

to

manage_payment_methods

rather than creating separate intents.

---

## 3. Is this merely a page-specific detail?

If the information is:

- one sentence
- one paragraph
- one option
- one UI element
- one feature under a broader workflow

Do NOT create a new intent.

Treat it as evidence for the broader intent.

---

## 4. Does this represent a genuinely different user goal?

Only propose ADD if ALL are true:

- it represents a distinct user objective
- it cannot naturally fit any existing intent
- it is likely to appear across multiple pages
- users would reasonably search for it independently
- merging it would reduce retrieval quality

Only then propose ADD.

---

# Strong Bias Against ADD

Adding intents increases:

- taxonomy size
- maintenance cost
- overlap
- ambiguity
- retrieval complexity

Therefore:

When uncertain,

prefer

- NO CHANGE
- MERGE
- RENAME

over ADD.

ADD should be the rarest proposal.

---

# Good Intent Characteristics

An intent should represent:

✔ a reusable user task

Examples:

- manage_subscription
- update_shipping_address
- manage_notifications
- request_refund
- track_order

Not:

- enable_sms_notification
- unsubscribe_newsletter
- change_restock_email
- toggle_marketing_emails

Those are all variations of a broader goal.

---

# When to Split

Only propose SPLIT if a single intent now covers multiple unrelated user goals.

Do NOT split simply because a page contains many details.

---

# When to Delete

Only propose DELETE when an intent is:

- obsolete
- duplicated
- fully absorbed into another intent

Never delete solely because it does not appear on the current page.

---

# Proposal Requirements

Every proposal must include:

- proposal type
- affected intent(s)
- supporting page evidence
- clear reasoning
- expected impact

Reasoning should explain **why the change improves the overall taxonomy**, not just the current page.

---

# Output

Produce:

- PAGE_INTENT_CHANGE_PROPOSALS
- STEP_1_CHECKS

---

# Validation Checklist

Before producing the output, verify:

✓ Every ADD was evaluated against all existing intents.

✓ Every ADD was rejected unless it represents a reusable independent user goal.

✓ Existing intents were preferred whenever reasonable.

✓ MERGE and RENAME were considered before ADD.

✓ No proposal is based solely on one isolated sentence or feature.

✓ Every proposal includes evidence and justification.

✓ STEP_1_CHECKS is complete.

---

# Final Flow

Present the generated PAGE_INTENT_CHANGE_PROPOSALS to the user for approval.

Never modify the taxonomy automatically.