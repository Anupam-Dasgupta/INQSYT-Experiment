# Notes

## General Observations About the Page

This page provides assistance and support options for managing or closing the Amazon account of a deceased customer. It explains the requirements for privacy/security (estate representative verification) and outlines options available based on the requester's access to the account credentials.

---

## Navigation Structure

The page is organized into three main sections:
- Protecting account information (outlines what can be done without full documentation, such as deactivation or stopping recurring deliveries/subscriptions).
- Having access to the email address or phone number associated with the account (guidance on signing in or resetting the password).
- Not having access to the account (verification documents required for requesting details, closing the account, or making changes).

---

## Page Quality Observations

The documentation is highly structured and clearly delineates support paths depending on the representative's level of access and legal documentation. It provides a direct email address (`bereavement-support-cs@amazon.com`) for submitting requests.

---

## Missing Documentation

The page does not specify:
- The expected response/processing time after emailing the bereavement support team.
- How to contact bereavement support for non-US marketplaces if the email address differs, or if this email is global.

---

## Missing Intents (Intentionally Excluded)

None identified. All support options and paths documented on the page have been represented under the final taxonomy.

---

## Retrieval Challenges

- High ambiguity between "deactivating the account" (which can be done with limited documents) and "closing the account" (which requires full estate representative verification). Users may confuse the two terms, so retrieval systems must map both to the appropriate access level instructions.
- The requirements list for verifying estate authority is lengthy and contains multiple distinct documents (death certificate, proof of estate authorization, photo ID, account identifier). These must be retrieved in full whenever a user asks about required documents.

---

## RAG Chunking Recommendations

Recommend splitting the content into three distinct chunks:
1. **Limited Bereavement Actions (No Authorization Docs)**: Covers the section on actions Amazon can assist with without full estate verification (terminating subscriptions, stopping deliveries, deactivating account) and the bereavement email address.
2. **Access-Based Management (With Credentials)**: Covers the procedure for signing in or resetting the password when the representative has access to the account's email/phone.
3. **Full Estate representative verification (Without Credentials)**: Covers the required documents and submission process for full account access, closure, or changes when access credentials are not available.

---

## Intent Ambiguity Observations

"Deactivating the account" (unauthorized) and "closing the account" (authorized) represent very similar end-goals but follow completely different paths and document requirements. Organizing them under the same super-intent `request_bereavement_support` but separating them by access/authorization status (`request_limited_bereavement_actions` vs `manage_account_without_access`) helps avoid ambiguity.

---

## Reusable Extraction Patterns

- Conditional support patterns: "If you [condition], we can still assist with: [list of actions]".
- Credential-based branching: "If you have access to [credentials], you can: [options]".
- Verification requirements list: "To [action] without having access, verification is required. To verify [attribute], we require the following: [list]".

---

## Taxonomy Design Observations

Created a single super-intent `request_bereavement_support` with three sub-intents (`request_limited_bereavement_actions`, `manage_account_with_access`, `manage_account_without_access`). This structure is based on the representative's access and authorization status, mirroring the three logical support paths provided on the source page.

---

## Edge Cases Noticed During Extraction

- Requesters can request subscription termination, delivery stoppage, or account deactivation with only the death certificate and the account email/phone (without full estate representation documents).
- If the associated email address is unknown, the requester must provide alternative identifiers like a unique charge ID or order number from a package, email, or statement.
- All documents sent to `bereavement-support-cs@amazon.com` are securely deleted after validation.

---

## Iteration 1 - Observations (2026-07-24)

- Extracted 8 granular candidate intents, which were reviewed and rejected in favor of a coarser, access/authorization-based hierarchy.
- Established the super-intent `request_bereavement_support` with three sub-intents: `request_limited_bereavement_actions`, `manage_account_with_access`, and `manage_account_without_access`.
- Outlined RAG chunking recommendations and documented retrieval challenges related to the distinction between deactivation and account closure.
