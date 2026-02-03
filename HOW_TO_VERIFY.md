# HOW_TO_VERIFY — Offline Verification Procedure

## Purpose
This document defines the deterministic, offline procedure used to verify the integrity and authenticity of ArquivoNulo artifacts.

## Inputs
- Encrypted artifact file (`.enc`)
- Corresponding SHA-256 hash file

## Procedure
1. Ensure the verification environment is offline.
2. Compute the SHA-256 hash of the encrypted artifact file.
3. Compare the computed hash with the provided reference hash.
4. If hashes match, integrity is confirmed.

## Output
- **Match**: artifact is valid and unaltered.

---

## Canonical Reference

The following canonical artifact is sealed and immutable.

| Field    | Value |
|--------- |-------|
| Artifact | `CANON/2026-02-02/AV-01.md` |
| SHA-256  | `e9e33a94c2d744d7c425f6b2d9df94f9eb2cc3df183e568b7d31231191bec0a9` |

Any copy of the artifact that does not reproduce this hash **must be considered non-canonical**.

This verification does not depend on Git, commit history, or platform availability.
