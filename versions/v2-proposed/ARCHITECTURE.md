# Candidate Screening v2.0 — Proposed Repair Architecture

> **Status:** PROPOSED REPAIR TARGET · not implemented.

```mermaid
flowchart TD
    A[Candidate intake] --> B[Validate required fields]
    B --> C[CV text extraction / supplied text]
    C --> D{Extraction confidence usable?}
    D -->|No| E[Failure record + retry / human path]
    D -->|Yes| F[Normalize candidate identity]
    F --> G[Authoritative duplicate lookup]
    G --> H{Existing candidate?}
    H -->|Yes| I[Return existing / duplicate response]
    H -->|No| J[Create and preserve candidate object]
    J --> K[Load job requirements]
    K --> L[Structured AI evaluation]
    L --> M[Schema validation + score clamping]
    M --> N[Merge evaluation with original candidate state]
    N --> O[Human review gate]
    O --> P[Audited persistence / final response]
```

## Design intent

The proposed v2 repair corrects the current branch inversion, replaces placeholder duplicate logic with an authoritative lookup, preserves a stable candidate envelope through AI evaluation, and introduces an explicit human-review/audit boundary.

This page is architecture **design evidence only**. It must not be described as implemented until a v2 workflow export and representative execution evidence exist.
