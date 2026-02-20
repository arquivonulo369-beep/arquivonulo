# HOW_TO_VERIFY — Offline Verification Procedure

## Purpose
This document defines the deterministic, offline procedure used to verify the integrity and authenticity of ArquivoNulo artifacts.

---

## Hash Standard

Artifacts created before 2026-02-12  
Algorithm: SHA-256  
Digest length: 64 hexadecimal characters (lowercase)

Artifacts created on or after 2026-02-12  
Algorithm: SHA3-384  
Digest length: 96 hexadecimal characters (lowercase)

The transition is forward-only.  
Legacy artifacts remain sealed under their original hash.

---

## Inputs
- Artifact file
- Corresponding hash sidecar file (`.sha256` or `.sha3-384`)

---

## Procedure
1. Ensure the verification environment is offline.
2. Identify the artifact creation date.
3. Determine the required hash algorithm.
4. Compute the hash of the artifact.
5. Compare the computed digest with the provided reference hash.
6. If hashes match, integrity is confirmed.

---

## Example (OpenSSL)

SHA-256:

openssl dgst -sha256 file.ext

SHA3-384:

openssl dgst -sha3-384 file.ext

---

## Output
- **Match**: artifact is valid and unaltered.
- **Mismatch**: artifact integrity cannot be confirmed.

---

## Canonical Reference (Pre-Transition Example)

The following canonical artifact is sealed and immutable under SHA-256.

| Field    | Value |
|--------- |-------|
| Artifact | `CANON/2026-02-02/AV-01.md` |
| SHA-256  | `e9e33a94c2d744d7c425f6b2d9df94f9eb2cc3df183e568b7d31231191bec0a9` |

Any copy of the artifact that does not reproduce this hash **must be considered non-canonical**.

This verification does not depend on Git, commit history, or platform availability.
