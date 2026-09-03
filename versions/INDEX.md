# Candidate Screening — Version / Generation Archive

This archive keeps historical execution, current defects and future repair plans separate.

- [Historical demonstrated generation](historical-demonstrated/README.md)
- [Current checked-in generation — under repair](current-under-repair/README.md)
- [Proposed v2.0 repair target](v2-proposed/README.md)

## Critical rule

The historical walkthrough must not be used to erase defects in the current checked-in JSON. Likewise, the v2 repair architecture must not be presented as implemented until a new workflow export and fresh execution evidence exist.

## Future promoted artifact

When v2 is actually implemented and tested, create a **new** workflow artifact named along the controlled pattern:

`Candidate_Screening_n8n_Workflow_v2.0_Repaired_<date>.json`

Never overwrite the current broken generation and then lose the repair history.