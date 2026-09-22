# Inputs template

## De-identified export

```
# Usage input set
Tool: {{TOOL}}    Period: {{PERIOD}}
Staff with access during period: {{ELIGIBLE_N}}   (from HR/roster, not the export)
Source of category field: [auto-classified by tool / self-reported / none]
Groups merged under {{MIN_CELL}}: [list]

user_id | role_group | building | conversations | active_weeks | top_category
U01 | Teacher | A | 142 | 17 | Teaching materials
...
```

`{{ELIGIBLE_N}}` matters: without it, you can describe users but not adoption. The export only contains people who used the tool.

## Summary table (for runs in any AI tool)

Compute these in a spreadsheet with conversations in column D and active weeks in column E (rows 2 to N+1). Paste the finished table, not the formulas.

| Figure | Google Sheets / Excel formula |
|---|---|
| Users in export | `=COUNTA(A2:A31)` |
| Staff with access | from roster |
| % of staff who used it at least once | users ÷ staff with access |
| Total conversations | `=SUM(D2:D31)` |
| Median conversations per user | `=MEDIAN(D2:D31)` |
| Top 10% of users: share of conversations | `=SUM(LARGE(D2:D31,{1,2,3}))/SUM(D2:D31)` (adjust count to 10% of users) |
| Stalled users (per `{{STALLED_DEF}}`) | `=COUNTIFS(D2:D31,"<=3",E2:E31,"<=2")` |
| Users and conversations by group | pivot table, groups at or above `{{MIN_CELL}}` only |
| Users by top category | `=COUNTIF(F2:F31,"Teaching materials")` etc. |

Adjust ranges to your data.

A caution the example teaches: if the category field is each user's *top* category, you can count users by top category. You cannot sum conversations by it and call that the distribution of conversation topics.
