---
type: Fixed
pr: 5044
---
**No shipped command, workflow or skill points at the absorbed `/gsd-add-phase` / `/gsd-insert-phase` any more** — eighteen lines in ten shipped files (including `/gsd:mvp-phase`'s "phase not found" hint and split list, `/gsd:phase`'s own usage message, and an `explore` instruction telling the model to invoke `/gsd-add-phase`) still named commands removed by the skill consolidation. They now name `/gsd:phase "<description>"` and `/gsd:phase --insert <after-phase> "<description>"`, and a guard that walks every shipped directory keeps all three spellings out. The MVP surfaces also spelled live commands as `/gsd <cmd>`, a form no runtime registers: twenty references to `/gsd plan-phase`, `/gsd mvp-phase` and `/gsd execute-phase` in nine shipped files, including `/gsd:mvp-phase`'s instruction to invoke `/gsd plan-phase`. They now use `/gsd:<cmd>`, and a second guard rejects that spelling for any live command. (#5002)
