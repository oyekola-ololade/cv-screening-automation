# Candidate Screening — Current Checked-In Generation

**Status:** **CURRENT · UNDER REPAIR · not buyer-ready**

## Current artifact

The checked-in generation is a real 13-node n8n workflow export. Inspection found useful implementation components alongside defects that invalidate an end-to-end “working demo” claim.

## Implemented/evidenced components

- candidate intake/webhook structure;
- supplied `cv_text` handling;
- requirement lookup / persistence components;
- structured AI-evaluation stage;
- explicit success/failure response nodes;
- update/persistence intent.

## Known defects

### 1. Extraction routing reversed
The current extraction decision routes valid extraction toward failure handling and can allow failed extraction to continue into screening.

### 2. Duplicate detection not authoritative
Duplicate logic is placeholder/hard-coded rather than a datastore-backed lookup.

### 3. State continuity risk
The candidate object/state is not robustly preserved across the AI-evaluation stage into downstream persistence/update behavior.

### 4. Input boundary
The current workflow expects supplied `cv_text`; binary PDF/image CV parsing is not proven by the checked-in generation.

## Current proof boundary

The workflow is useful engineering evidence because the defect diagnosis is inspectable. It must not be represented as a current verified recruiter workflow until repaired and rerun.

## Media

Current-version placeholders:

- [`../../evidence/current/demo/README.md`](../../evidence/current/demo/README.md)
- [`../../evidence/current/screenshots/README.md`](../../evidence/current/screenshots/README.md)

The existing `../../assets/current-vs-target.svg` is architecture/diagnostic evidence, not runtime proof.