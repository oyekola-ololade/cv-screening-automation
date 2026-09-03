# Candidate Screening — Repository Index

> **Current truth:** partial 13-node n8n implementation under repair. A historical walkthrough demonstrated an earlier working flow, but the current checked-in export contains known routing/state defects and must not be called a working end-to-end demo.

## Start here

- [Main README](README.md)
- [Version / generation archive](versions/INDEX.md)
- [Current-vs-target visual](assets/current-vs-target.svg)
- [Repair specification](docs/REPAIR_PLAN.md)
- [Test plan](docs/TEST_PLAN.md)
- [Security policy](SECURITY.md)
- [Changelog](CHANGELOG.md)
- current under-repair workflow export in the repository root/workflow path

## Lineage

| State | Meaning | Status |
|---|---|---|
| Historical demonstrated generation | earlier screening flow shown in a walkthrough | historical execution evidence |
| Current checked-in generation | 13-node export with known defects | **CURRENT · UNDER REPAIR** |
| v2.0 repair target | defined corrected architecture/data/human-review contract | PROPOSED · not implemented yet |

See [`versions/`](versions/INDEX.md) for detailed records.

## Current known defects

- extraction decision routing is reversed;
- duplicate detection is placeholder/hard-coded rather than an authoritative lookup;
- candidate state is not reliably preserved through the AI stage into final persistence;
- current flow expects supplied `cv_text`; binary CV parsing is not proven.

## Media rule

Only the **current under-repair generation** gets missing-media placeholders:

- [Current demo placeholder](evidence/current/demo/README.md)
- [Current screenshot placeholder](evidence/current/screenshots/README.md)

The historical walkthrough remains historical; the proposed v2 target does not get fake demo/screenshots before it is actually implemented.