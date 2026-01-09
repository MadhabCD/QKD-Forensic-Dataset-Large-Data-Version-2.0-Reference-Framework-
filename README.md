# QKD-Forensic Dataset V2.0  
**Anomaly and Intrusion Detection in Quantum Key Distribution Using Integrated Quantum and Classical Measurements**
**Download:**

DOI: 10.5281/zenodo.18195501

---

## Overview

This repository contains the **framework, documentation, and data generation scripts** for  
**QKD-Forensic Dataset V2.0**, an advanced research dataset designed for:

- Anomaly detection in Quantum Key Distribution (QKD)
- Intrusion detection across quantum and classical layers
- Machine learning–based forensic analysis of QKD systems

The dataset integrates **quantum-layer measurements** (e.g., QBER, decoy-state statistics) with  
**classical network and system-level measurements**, enabling multi-layer security analysis.

---

## Relationship to Previous Version (V1.0)

This is **Version 2.0** of the dataset.

- **Version 1.0 (Published, Archived, DOI Assigned):**  
  - Zenodo: https://zenodo.org/records/17773084  
  - GitHub: https://github.com/MadhabCD/QKD-Forensic-Dataset  

### Key differences from V1.0:
- Expanded feature space (quantum + classical integration)
- Time-indexed, per-second sampling
- Explicit attack and fault scenario modeling
- Improved reproducibility via centralized configuration
- Designed for deep learning and temporal models (LSTM, CNN, HMM, etc.)

Version 1.0 remains **unchanged and citable**.  
Version 2.0 is a **new, extended dataset**, not a replacement.

---

## Research Scope

This dataset supports research in:

- Quantum cybersecurity
- QKD anomaly and intrusion detection
- Quantum-aware digital forensics
- Machine learning and deep learning for security
- Cross-layer attack attribution (quantum vs classical)

---

## Scenarios Modeled

The dataset includes the following operational conditions:

1. **Normal Operation**
2. **Eavesdropping (Intercept–Resend style)**
3. **Channel Degradation (Benign Fault)**
4. **Classical Network DoS**
5. **Misconfiguration / Timing Drift**

Each scenario is modeled independently with consistent time indexing.

---

## Time Indexing

- Sampling interval: **1 second**
- Each row represents one second of system behavior
- All data streams are aligned using an integer `timestamp`

Details:  
See `docs/TIME_AXIS.md`

---

## Feature Categories
- Note: Not all listed signals are provided as raw measurements; several are
represented as aggregated or derived features in the released dataset.

### Quantum Measurements
- QBER (Z and X bases)
- Signal and dark count rates
- Sifted and secure key estimates
- Decoy-state gains
- Timing jitter and basis mismatch
- Channel loss and polarization drift

### Classical Measurements
- Network RTT, packet loss, throughput
- Firewall drops
- System log warnings and errors
- NTP offset and jitter
- CPU and memory usage
- Control message drops
- Routing changes and handshake failures

Full definitions:
- `docs/MODELING/QUANTUM_MODEL.md`
- `docs/MODELING/CLASSICAL_MODEL.md`

---

## Repository Contents (GitHub)

This GitHub repository contains **only**:

- Dataset documentation
- Configuration files
- Data generation scripts

**Raw and processed CSV data are NOT stored in GitHub.**  
They are released separately via Zenodo for archival and citation purposes.

---

## Reproducibility

- Centralized configuration: `config/global_config.yaml`
- Fixed random seed (`seed = 42`) for deterministic generation
- The provided scripts implement a reproducible reference framework that illustrates
how quantum and classical signals are modeled and aligned. They are not intended
to regenerate the released dataset bit-by-bit.

---

## Data Availability

- **Full Dataset (CSV):** Released via Zenodo (V2.0 DOI will be provided upon publication)
- **Scripts & Documentation:** Available in this GitHub repository

---

## Citation

If you use **QKD-Forensic Dataset V2.0**, please cite:

> Madhab Chandra Das, *QKD-Forensic Dataset V2.0: An Integrated Quantum–Classical Dataset for Anomaly and Intrusion Detection in QKD Systems*, 2026.

(Full BibTeX and DOI will be added after Zenodo publication.)

For Version 1.0, please cite the original dataset:
- DOI: https://zenodo.org/records/17773084

---

## License

This project is released under the license specified in the `LICENSE` file.

---

## Contact 
**Madhab Chandra Das** 
Graduate Research Assistant, Digital & Cyber Forensics
Sam Houston State University 
Email: mxd147@shsu.edu & madhabdas.2109@gmail.com ---

 ## Research Disclaimer 
 
 This dataset and framework are intended **strictly for defensive, academic, and research purposes**, including the study of vulnerabilities and resilience mechanisms in quantum communication systems.
## Notes

This repository is part of an ongoing research program.  
Future releases may include:

- Larger-scale datasets
- Extended feature sets
- Advanced attack models
- SCI-journal dataset extensions

