# Candidate Screening — Current Checked-In Architecture

> **Status:** CURRENT · UNDER REPAIR · diagnostic architecture, not a successful-runtime diagram.

```mermaid
flowchart TD
    A[Webhook / candidate submission] --> B[Receive supplied cv_text]
    B --> C[Extraction / structure]
    C --> D{Extraction decision}
    D -->|Current misroute| E[Failure handling]
    D -->|Current opposite branch| F[Continue screening]
    F --> G[Duplicate decision]
    G --> H[AI evaluation]
    H --> I[Persist / update]
    I --> J[Webhook response]

    D -. Known defect: success/failure routing reversed .-> K[Routing defect]
    G -. Known defect: placeholder / hard-coded duplicate result .-> L[Duplicate defect]
    H -. Known risk: candidate state not robustly preserved .-> M[State-continuity risk]
```

## Current defects represented

1. **Extraction routing is reversed.**
2. **Duplicate detection is not authoritative.**
3. **Candidate state continuity is unreliable after AI evaluation.**
4. The workflow expects supplied `cv_text`; binary document extraction is not proven.

The repository-level `assets/current-vs-target.svg` and this page describe the same current defect boundary. Neither is runtime success evidence.
