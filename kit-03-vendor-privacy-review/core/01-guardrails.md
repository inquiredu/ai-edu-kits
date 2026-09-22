# Guardrails

## Tool lane
Vendor contracts and DPAs are usually not confidential, but some contain pricing, security details, or confidentiality clauses. Check the contract's own confidentiality terms before pasting it into any tool. Negotiation notes, legal memos, and attorney communications stay out unless counsel agrees. No student data is needed for this kit, and none should be included.

## Statuses

| Status | Meaning |
|---|---|
| **Addressed** | Contract language directly addresses the requirement, and the quoted text matches it |
| **Partial** | Addresses part of the requirement, or uses weaker terms |
| **Conflicts** | Contract language points in a different direction from the requirement |
| **Not found** | No relevant language located in the documents provided |
| **Counsel review** | Language exists, but whether it satisfies the requirement is a legal judgment |

The statuses describe the relationship between two texts. None of them is a legal conclusion. "Addressed" does not mean "compliant."

## What the AI roles may and may not do

| May | May not |
|---|---|
| Locate and quote contract language | State that a vendor is compliant or in violation |
| Compare language against your requirements file | Supply legal requirements from memory |
| Note where terms are weaker, vaguer, or conflicting | Recommend signing or not signing |
| Draft questions for vendor and counsel | Draft binding contract language as final |

## Documents that override each other
Vendor terms often say which document controls in a conflict (DPA over terms of service, or the reverse). The Extractor finds that clause first. A strong DPA can be undercut by an order-of-precedence clause.
