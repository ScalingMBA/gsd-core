---
type: Fixed
pr: 5043
---
**Quick-task rows and audit acknowledgements are dated with your local day, and honour the test clock pin** — `quick-tasks-append` (the Date column of STATE.md's Quick Tasks Completed table) and `audit-open acknowledge` without `--at` took the UTC calendar day of the real wall clock, so work done between local midnight and UTC midnight was stamped with the wrong day, and `GSD_NOW_MS` could not pin either value. Both now use the local calendar day through the clock seam, like every other operator-facing date field; an explicit `--at` still wins. (#4905)
