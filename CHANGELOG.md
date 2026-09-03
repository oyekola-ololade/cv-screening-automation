# Changelog

## 2026-09-03 — Repair-state evidence hardening

### Changed

- Replaced the stale visual project page that implied a reliable success path with an under-repair diagnostic page.
- Updated the README to classify the current export as a partial implementation under repair.
- Embedded a current-vs-target architecture visual.

### Added

- `docs/REPAIR_PLAN.md`
- `docs/TEST_PLAN.md`
- `SECURITY.md`
- `assets/current-vs-target.svg`

### Current blocking defects

- extraction routing is reversed;
- duplicate detection is placeholder logic rather than authoritative lookup;
- candidate state is not reliably preserved through AI evaluation into final persistence.

### Boundary

No repaired v2 workflow or passing runtime test result is claimed by this release. Reclassification requires an actual repaired export plus representative configured test evidence.
