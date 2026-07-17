# Notes

## General Observations About the Page

The page details guidelines for identifying and avoiding internet payment scams, phishing attempts, and fraudulent sellers on Amazon. It provides clear, actionable "do's and don'ts" rules for buyers to ensure secure checkout transactions.

---

## Navigation Structure

The page is organized into the following sections:
1. Header: "Avoiding Payment Scams"
2. Introductory warning on protecting yourself from fraud.
3. List of core safety rules to prevent scams (paying through Amazon, avoiding wire transfers, ignoring scam payment requests).
4. Direct links to external/supplemental pages for email identification and gift card scams.

---

## Page Quality Observations

The safety rules are highly structured and use clear, imperative language ("Don't wire money", "Don't make a payment to claim a prize"). The integration of warning links for gift card fraud and fake emails provides good safety coverage.

---

## Missing Documentation

The page does not explain how a user should report a scammer if they have already fallen victim or encountered a suspicious seller, though it links to email identification.

---

## Missing Intents (Intentionally Excluded)

None. The single intent `avoid_payment_scams` covers all the security and scam-avoidance guidelines described.

---

## Retrieval Challenges

Queries such as "how do I know if this seller is a scammer", "is this email a scam", "can I pay off-site", or "wired money to seller" must retrieve this safety advice. Mapping diverse phrasing for fraud (phishing, spoofing, scam) is important.

---

## RAG Chunking Recommendations

We recommend chunking this document into two chunks:
1. Core Scam Avoidance Rules: The list of bullet points detailing safety practices.
2. Scam Resources & Links: The warnings and links regarding fake emails and gift card fraud.

---

## Intent Ambiguity Observations

There is low ambiguity. Safety and fraud prevention is a distinct category from transactional payment issues (declines, unrecognized charges).

---

## Reusable Extraction Patterns

- "Protect yourself from fraud on the internet by..."
- "To avoid payment scams: ..."
- "Don't do business with a seller who..."

---

## Taxonomy Design Observations

Consolidated all phishing warnings, payment security rules, and external scam links under the single intent `avoid_payment_scams` to prevent a fragmented taxonomy.

---

## Edge Cases Noticed During Extraction

- Sellers attempting to direct customers to complete transactions off the Amazon website.
- Requesting payment via wire transfer, cash, or gift cards.
- Requests for payment in order to claim prize winnings or verify identity.

---

## Iteration 1 - Observations (2026-07-17)

- **Important extraction observations**: Safety-critical advice with strict action warnings regarding off-site transactions and wire transfers.
- **Approved taxonomy changes**: Added the intent `avoid_payment_scams`.
- **Rejected taxonomy changes**: None.
- **Retrieval observations**: Highly likely that users seeking safety confirmation before a transaction or reporting a suspicious seller will search for this page.
- **Taxonomy decisions**: Grouped all fraud, scam, and phishing warnings under a single security intent.
- **Chunking observations**: Keeping the list of rules together is critical to preserve the relational checklist context.
- **Notable edge cases**: Off-site seller transaction requests.
- **Lessons useful for future pages**: Security and fraud prevention guidelines are best served as comprehensive, single-intent reference pages.
