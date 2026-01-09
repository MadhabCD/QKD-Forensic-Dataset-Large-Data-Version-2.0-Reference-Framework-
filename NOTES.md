# Internal Research Notes — QKD-Forensic Dataset V2.0

This file records internal design decisions and versioning notes
for the QKD-Forensic Dataset V2.0 project.

It is intentionally concise and non-redundant with README.md.

---

## Dataset Lineage

- **Version 1.0**
  - Publicly released and archived
  - DOI: https://zenodo.org/records/17773084
  - GitHub: https://github.com/MadhabCD/QKD-Forensic-Dataset

- **Version 2.0 (This Repository)**
  - New dataset generation framework
  - Expanded feature space
  - Time-indexed, per-second sampling
  - Designed for multi-layer anomaly and intrusion detection

Version 2.0 is an **extension**, not a modification, of Version 1.0.

---

## Design Principles

- Separation of concerns:
  - Documentation (docs/)
  - Configuration (config/)
  - Data generation scripts (scripts/)
  - Data storage (Zenodo only)

- Reproducibility:
  - Fixed random seed (seed = 42)
  - Centralized configuration via YAML
  - Deterministic generation logic

- Transparency:
  - Explicit modeling assumptions
  - Scenario-wise behavior definitions
  - Clear time alignment rules

---

## Scope Clarification

- This GitHub repository does NOT host raw or processed dataset CSV files.
- Full datasets are released via Zenodo for archival and citation.
- GitHub is used strictly for:
  - Documentation
  - Scripts
  - Configuration
  - Reproducibility support

---

## Versioning Policy

- GitHub repository tracks framework evolution.
- Zenodo releases are immutable and citable.
- Future versions (e.g., V2.1, V3.0) will be released as separate Zenodo records.

---

## Intended Use

This dataset framework is intended for:
- Academic research
- Reproducible experiments
- Benchmarking anomaly and intrusion detection models

It is not intended for deployment in production QKD systems.

---

## Author Note

This file exists to support long-term research continuity and
should not be cited as a primary dataset description.

Refer to README.md for official dataset documentation.
