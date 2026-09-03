# Candidate Screening v2.0 — Proposed Repair Target

**Status:** PROPOSED / REPAIR TARGET · **not implemented**

## Target architecture

The repair specification defines a corrected flow around:

1. candidate intake;
2. input validation;
3. CV text extraction or supplied text;
4. extraction-confidence gate;
5. normalized candidate identity;
6. authoritative duplicate lookup;
7. preserved candidate object/state;
8. structured AI evaluation with schema validation;
9. human-review gate;
10. audited final persistence/response.

## Required repair outcomes

### Extraction
Valid extraction proceeds into screening; failed/low-confidence extraction creates an explicit failure/retry/human path.

### Duplicate detection
Replace hard-coded/placeholder duplicate behavior with an authoritative lookup and explicit duplicate response.

### State continuity
Carry a stable candidate envelope through AI evaluation and downstream persistence instead of reconstructing state ambiguously from model output.

### Human review
High-impact or uncertain decisions remain reviewable and auditable rather than being silently finalized by the model.

### Security/data handling
CV/candidate data needs explicit retention/access/publication controls before production-like use.

## Promotion gate

Do not rename this folder or project status to `implemented` until all exist:

- new v2 workflow export;
- branch tests;
- current screenshots/execution evidence;
- architecture diagram matching the implemented graph;
- limitations/security section;
- buyer-proof packet updated to v2.

## Media

Proposed version. No fake demo/screenshot placeholders until it becomes the current implemented generation.