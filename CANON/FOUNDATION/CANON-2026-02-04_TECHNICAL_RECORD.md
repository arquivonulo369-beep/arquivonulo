# ArquivoNulo — Technical Record

CANON Date: 2026-02-04T00:00:00Z

## 1. Scope
This document defines a forensic protocol for sovereign registration
of AI system states, independent of vendors, platforms, or carriers.

## 2. Core Definitions

### Boundary
Formal delimitation of the system, model, dataset, or process under observation.
Defines what is inside and what is outside the forensic scope.

### Baseline
A cryptographically hashed reference state established at a specific CANON time.
Serves as the immutable point of comparison.

### Evidence Cell
An isolated and immutable forensic unit preserving a deviation, event,
or state change relative to a Baseline.

### Tríptico Forense
The minimal forensic structure composed of:
Boundary + Baseline + Evidence Cell.

### CANON
A semantic and temporal freeze establishing anteriority.
Prevents retroactive modification or reinterpretation of state.

### No-Carrier Neutrality
Only cryptographic hashes are anchored.
No raw data, no custody, no dependency on storage providers or platforms.

## 3. Verification
All records generated under this protocol are verifiable offline
through SHA-256 hash comparison against publicly anchored references.
