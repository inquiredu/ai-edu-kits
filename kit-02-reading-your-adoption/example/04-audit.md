# Audit (synthetic example)

## A. Flags

| # | Severity | Location | As written | What the data shows | Smallest fix |
|---|---|---|---|---|---|
| 1 | HIGH | Reach | "adoption is growing steadily across the semester" | The export has one period and no dates per conversation. No trend can be computed. | Delete. If trend matters, compare the same export next period. |
| 2 | HIGH | Concentration | "These heavy users are clearly saving the most time." | No field measures time. Conversation counts measure frequency. | Delete, or: "Whether frequent use reflects time saved is a question to ask these users directly." |
| 3 | HIGH | Groups | "Two of the three other staff at Building B stalled." | Crossing role with building produces a group of 3, below the minimum of 5. In a small building this can identify people. | Remove the breakdown. Report stalls overall, or by building only. |
| 4 | MEDIUM | Categories | "55% of all conversations were about teaching materials." | The category field is each user's single top category. Summing conversations by it (365 of 664) does not describe what conversations were about. | "11 of 30 users' most frequent category was teaching materials; 10 communication; 9 subject Q&A." |
| 5 | MEDIUM | Buildings | "Building B staff are less engaged…" | Medians are correct (6 vs. 9), but staff with access by building is not available, so reach can't be compared, and "engaged" is not a measured quantity. | "Among users, Building B's median was 6 conversations and Building A's was 9. Reach by building can't be compared without roster counts." |
| 6 | LOW | Stalled | "opened the tool and stopped" | Accurate under the definition; worth stating the definition inline. | Add "(3 or fewer conversations, active 2 or fewer weeks)." |

## B. Figure check

| Figure | Stated | Verified | Source |
|---|---|---|---|
| Reach | 30 of 70, 42.9% | 30 of 70, 42.9% | table |
| Top-3 share | 47.6% | 316 / 664 = 47.6% | table |
| Stalled | 11 of 30, 36.7% | 11 of 30, 36.7% | table |
| Building medians | 6 and 9 | 6 and 9 | table |
| Teaching-materials "share" | 55% | 365 / 664 = 55.0%, but invalid at this grain | recomputed from export |
| Other staff at B stalled | 2 of 3 | 2 of 3 (U22, U25), but suppressed | recomputed from export |

Every number in the first pass was arithmetically correct. Every HIGH flag came from what the numbers were made to mean. That is the usual pattern.

## C. Verdict
**Ready after listed fixes.** The figures hold; the claims don't. Fixes 1–5 are deletions or rewordings that need no new analysis.

## D. Questions for the decision owner
- Eleven people tried and stopped. Would a short conversation with a few of them (Kit 04) tell you more than any further analysis of this export?
- Can you obtain staff-with-access counts by building before the next read?
