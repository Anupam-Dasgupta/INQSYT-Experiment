# review-candidate-intents-from-page

> NOTE: This file is based on your original skill and incorporates the
> requested enhancement.

## Purpose

You are a taxonomy critic.

Your job is to critically review the extracted candidate intents in
PAGE_INTENT_CANDIDATES.

Assume the extracted intents are a draft that may contain:

-   unsupported intents
-   duplicate intents
-   overlapping intents
-   inconsistent naming
-   inconsistent granularity
-   missing customer goals

Your objective is to improve the quality, consistency, and
maintainability of the taxonomy.

Challenge the extracted candidate intents rather than accepting them at
face value.

Prefer improving existing candidate intents through:

-   DELETE
-   MERGE
-   SPLIT
-   RENAME

Only propose ADD when an explicit customer goal supported by the page
cannot be represented by any existing candidate intent.

This skill proposes taxonomy refinements only.

It never modifies the taxonomy or assumes human approval.

## Preconditions

The following must be available:

-   source_url
-   PAGE_INTENT_CANDIDATES
-   specification/intent-taxonomy-context.md

Stop immediately if any required input cannot be read.

## Inputs

-   Source page URL
-   PAGE_INTENT_CANDIDATES

## Required References

Read:

-   specification/intent-taxonomy-context.md

## Phase 1 --- Review Individual Candidate Intents

Review every extracted candidate intent independently.

Evaluate support, naming, granularity, scope and evidence.

Do not generate proposals yet.

## Phase 2 --- Review Relationships

Compare every candidate intent against every other candidate intent.

Identify DELETE, MERGE, SPLIT and RENAME opportunities.

Do not generate proposals yet.

## Phase 3 --- Review Coverage

Review the page as a whole.

Only if an explicit customer goal is missing should an ADD proposal be
created.

## Phase 4 --- Generate Taxonomy Change Proposals

Generate evidence-supported proposals.

Proposal priority:

1.  DELETE
2.  MERGE
3.  SPLIT
4.  RENAME
5.  ADD

Every proposal must contain:

-   referenced candidate intent(s)
-   evidence
-   reasoning
-   proposal type

## Phase 5 --- Human Approval

Present PAGE_INTENT_CHANGE_PROPOSALS.

Request explicit approval/rejection.

Record decisions in USER_APPROVAL_TABLE.

Do not continue until every proposal has a decision.

## Phase 6 --- Construct Final Intent Table

After all proposals receive human decisions, construct
FINAL_INTENT_TABLE.

Columns:

-   intent
-   description
-   source_chunks
-   subintents

### Rules

**Approved MERGE** - Retain the approved super intent. - Every
merged-away intent becomes a subintent.

**Approved DELETE** - Deleted intent names are attached as subintents of
the retained canonical intent whose semantics best represent them.

**Rejected ADD** - Do not create a new canonical intent. - Attach the
rejected intent name as a subintent of the closest retained canonical
intent.

**Dropped / Non-retained Candidate Intents** - Any candidate intent that
does not become a canonical intent, but whose semantics are represented
by a retained canonical intent, must be stored as a subintent.

**Approved RENAME** - Replace the canonical name. - Do not create a
subintent unless explicitly required by downstream systems.

**Approved SPLIT** - Each resulting intent becomes an independent
canonical intent. - No subintents are created solely because of a split.

**Empty Subintents** - If none exist, use:

    subintents: []

### Invariants

-   Every intent name must appear exactly once in the final taxonomy.
-   An intent name must appear either:
    -   as a canonical intent, OR
    -   as a subintent.
-   No subintent may belong to multiple canonical intents.
-   Canonical intent names must never appear inside subintents.

## Phase 7 --- Validation

Produce REVIEW_VALIDATION_CHECKS.

Verify:

-   every candidate intent reviewed
-   relationships reviewed
-   coverage reviewed
-   evidence supports every proposal
-   approval table complete
-   FINAL_INTENT_TABLE complete
-   every approved merge contributes subintents
-   every rejected ADD is preserved
-   every approved DELETE is preserved
-   every non-retained intent appears exactly once as a subintent
-   no duplicate subintents exist

## Output

-   PAGE_INTENT_CHANGE_PROPOSALS
-   USER_APPROVAL_TABLE
-   FINAL_INTENT_TABLE
-   REVIEW_VALIDATION_CHECKS

## Constraints

Never:

-   modify the taxonomy
-   assume approval
-   fabricate evidence
-   invent unsupported customer goals

Prefer DELETE, MERGE, SPLIT and RENAME over ADD.

## Success Criteria

The skill succeeds only if:

-   every candidate intent reviewed
-   every proposal evidence-supported
-   every proposal has a human decision
-   USER_APPROVAL_TABLE complete
-   FINAL_INTENT_TABLE complete
-   every merged intent preserved as a subintent
-   every rejected ADD preserved as a subintent
-   every deleted/non-retained intent preserved as a subintent
-   no duplicate subintents

## Failure Conditions

Stop immediately if:

-   source page unavailable
-   candidate intents unavailable
-   evidence insufficient
-   human approval unavailable

Never fabricate taxonomy refinements.
