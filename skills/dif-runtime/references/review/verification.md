# Verification Protocol

Use this protocol in review and validation workflows.

## Status

- VERIFIED — requirement was directly inspected and evidence supports it.
- FAILED — requirement was directly inspected and evidence shows a violation.
- NOT VERIFIED — relevant, but available evidence cannot establish the result.
- NOT APPLICABLE — requirement does not apply to the inspected scope.

Never report VERIFIED without direct evidence.

## Evidence

For every finding record:
- scope/location;
- observed evidence;
- requirement or expected behavior;
- impact;
- recommended correction.

Do not infer runtime behavior from static appearance when execution determines the result.

## Root Cause Consolidation

One root cause equals one finding.
Group confirmed occurrences under the same finding instead of duplicating symptoms.

## Severity

- Critical — blocks task completion, creates serious accessibility/safety/data-loss risk, or invalidates the requested outcome.
- High — significant user or implementation impact.
- Medium — meaningful degradation in comprehension, efficiency, adaptability or consistency.
- Low — isolated issue with limited impact.
- Observation — relevant information without a confirmed defect.
