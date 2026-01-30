# LEGAL_FRAMEWORK_TIER2_DATASET.md

## Purpose
This document defines the legal and technical framing of the **Tier 2 Dataset** as a verifiable external reference for AI governance and compliance activities.

## Artifact Description
The Tier 2 Dataset is a sealed, append-only collection of encrypted cells containing higher-resolution records of system trade-offs, calibration decisions, and documented failure patterns.

The dataset is immutable after release and does not support updates, retraining, or adaptive feedback loops.

## Regulatory Alignment
The dataset provides documentary support for:

- **EU AI Act – Article 9 (Risk Management):**  
  Supplies frozen evidence of identified and evaluated risks used in system design and assessment.

- **EU AI Act – Article 10 (Data Governance):**  
  Acts as an external provenance reference for data-related decisions without modifying internal datasets.

- **ISO/IEC 22989:2022 – Clause 5.2:**  
  Supports governance transparency and lifecycle documentation through immutable records.

- **Audit & Assurance Use:**  
  Enables auditors to reference third-party, non-editable material when assessing compliance claims.

## Legal Characterization
- Non-operational dataset  
- No API, no telemetry, no monitoring  
- Offline verification only  
- Suitable for internal audit, external audit, and regulatory review

## Verification
All cells are encrypted and verifiable via deterministic cryptographic procedures documented in `HOW_TO_VERIFY.md`.  
Identical verification results are produced regardless of time or environment.

## Liability Boundary
The Tier 2 Dataset does not replace internal controls or risk management systems.  
It serves solely as external reference material.

Use of this dataset does not constitute endorsement, certification, or regulatory approval by ArquivoNulo.
