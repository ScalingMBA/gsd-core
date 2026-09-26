---
type: Fixed
pr: 5014
---
**Decision-coverage gates no longer honor an unsupported top-level `context_coverage_gate`** — `check.decision-coverage-plan` and `check.decision-coverage-verify` fell back to a flat `context_coverage_gate` key that `config-set` rejects and the config loader warns it ignores. A config with only `"context_coverage_gate": false` therefore made the blocking plan-phase gate silently pass with uncovered decisions while `config-get workflow.context_coverage_gate` reported the gate enabled. Both gates now read `workflow.context_coverage_gate` only — set that key to disable them.
