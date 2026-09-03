# Candidate Screening Test Plan

## Status

This is the acceptance-test plan for the repaired v2 target. **No PASS result is claimed until a repaired workflow is implemented and executed.**

## Routing

| Case | Expected |
|---|---|
| Valid supplied `cv_text` | success/screening branch |
| Empty CV text | failure/review branch |
| Very short/insufficient text | failure/review branch |
| Malformed webhook payload | deterministic validation error |

## Duplicate handling

| Case | Expected |
|---|---|
| New normalized email | candidate can be created |
| Existing normalized email | duplicate/existing response; no second record |
| Same request replayed | no unintended duplicate side effect |
| Duplicate store unavailable | safe failure; do not assume "not duplicate" |

## AI output

| Case | Expected |
|---|---|
| Valid structured JSON | schema validation succeeds |
| Invalid JSON | no candidate evaluation overwrite |
| Missing required field | validation error / review |
| Score below 0 / above 100 | reject or clamp according to explicit contract |
| Model/provider error | safe failure path |

## Candidate-state continuity

The test must prove the original candidate identifier, normalized email, source data, and record reference remain available after AI evaluation and point to the same candidate when the final update executes.

## Persistence

- append/create writes the intended candidate once;
- update writes the intended evaluation to that same candidate;
- failed extraction does not accidentally enter the success update route;
- duplicate candidates are not inserted;
- error paths do not report success.

## Human-review boundary

Representative tests should include a low-confidence or ambiguous case that remains reviewable by a person. The workflow must not be presented as autonomous hiring.

## Evidence to capture after repair

- repaired workflow JSON;
- test inputs using synthetic data;
- n8n execution screenshots or exported execution evidence for representative success/failure/duplicate cases;
- final TEST_RESULTS.md with date, environment, cases executed, actual result, and known limitations.
