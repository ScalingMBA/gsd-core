---
type: Fixed
pr: 5041
---
**The debugger's knowledge base is no longer reported or listed as a debug session** — `gsd-debugger` appends every resolved session to `.planning/debug/knowledge-base.md`, and `audit-open`, `/gsd-debug list` and the debugger's own active-session check all treated that file as a session: `audit-open` reported it as open on every run (so every milestone-close audit carried a permanent false positive), and `/gsd-debug list` showed it and offered it for resume. All three now skip it by name. `/gsd-debug list` also no longer hides a real active session whose slug contains "resolved" (e.g. `unresolved-promise-hang`). (#4869, #5011)
