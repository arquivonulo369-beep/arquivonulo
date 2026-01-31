# HOW_TO_VERIFY — Offline Verification Procedure

## Purpose
This document defines the deterministic, offline procedure used to verify the integrity and authenticity of ArquivoNulo artifacts.

## Inputs
- Encrypted artifact file (.enc)
- Corresponding SHA-256 hash file

## Procedure
1. Ensure the verification environment is offline.
2. Compute the SHA-256 hash of the encrypted artifact file.
3. Compare the computed hash with the provided reference hash.
4. If hashes match, integrity is confirmed.

## Output
- Match: artifact is valid and unaltered.
