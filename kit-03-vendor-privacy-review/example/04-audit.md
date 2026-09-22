# Audit (synthetic example)

## A. Flags

| # | Severity | Location | As written | What the documents and requirements show | Smallest fix |
|---|---|---|---|---|---|
| 1 | HIGH | MN-4 | Status "Addressed" | §7.2: "delete Student Data within 180 days." MN-4: within 90 days of expiration. The terms point in different directions. The first-pass quote also cut off the timeframe. | Status → Conflicts. Quote §7.2 in full. |
| 2 | HIGH | MN-3 | "Minnesota requires breach notice within 72 hours" | MN-3, as provided, requires disclosure of information needed to meet § 13.055. It states no 72-hour deadline. (The requirements file's only 72-hour item, MN-11, concerns device access under the imminent-threat exception and does not apply here.) | Remove the deadline. Relate the texts: §6.2 commits to notice "within a commercially reasonable time" and information "reasonably requested," which is narrower than "all information necessary." Status → Partial or Counsel review. |
| 3 | HIGH | MN-3 | "BrightPath is in violation of state law" | A legal conclusion. The kit maps texts; counsel decides. | Delete. |
| 4 | MEDIUM | MN-6 | Status "Addressed" | MN-6 allows de-identified aggregate use to improve the provider's own service. §4.3 also permits sharing de-identified data "with research partners," which the requirement's carve-out does not mention. §4.1 prohibits "targeted advertising," narrower than "marketing or advertising." | Status → Counsel review. Quote §4.1 and §4.3 in full. |
| 5 | LOW | MN-7 | — | Status Partial is supported. | None. |

## B. Quote check

| Quote | Verbatim? | Section correct? |
|---|---|---|
| §2.1 | Yes | Yes |
| §6.2 fragment | Yes, partial | Yes |
| §7.2 "BrightPath will delete Student Data" | Truncated — omits "within 180 days" and "Upon termination" | Yes |
| §4.1, §4.3 fragments | Yes, partial | Yes |
| §3.1 | Yes | Yes |

## C. Status check

| ID | Stated | Supported? | Note |
|---|---|---|---|
| MN-2 | Addressed | Yes | |
| MN-3 | Conflicts | No | Partial or Counsel review; see flags 2–3 |
| MN-4 | Addressed | No | Conflicts; see flag 1 |
| MN-6 | Addressed | No | Counsel review; see flag 4 |
| MN-7 | Partial | Yes | |

Precedence: §1.1 makes the DPA control over the Terms of Service. The Terms were not provided, so any stronger or weaker terms there are unknown. Worth requesting.

## D. Verdict
**Re-run analysis.** Two statuses are wrong in ways that would lead a reader to think the contract meets requirements it conflicts with, and the review contains a legal conclusion and an invented deadline.

## E. Items for counsel the review may have missed
- Whether "research partners" in §4.3 falls within MN-6's carve-out, or within MN-5 (not in this subset).
- Whether "confirmed security incident" in §6.2 aligns with a breach "as defined in § 13.055."
- Whether BrightPath meets the subd. 1(g) definition of "technology provider."
