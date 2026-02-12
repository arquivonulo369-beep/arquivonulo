# SIA Hash Standard — 2026 Transition Layer

Date: 2026-02-12  
Status: Declarative

## 1. Scope

This document records the hash function applied to artifacts created on or after 2026-02-12 inside the SIA structure.

## 2. Standard

Algorithm for artifacts created on or after 2026-02-12:  
SHA3-384 (384-bit output)

Algorithm for legacy artifacts (pre-2026-02-12):  
SHA256 (preserved as originally computed)

## 3. Non-Retroactivity Principle

Artifacts sealed before 2026-02-12 are not:  
- re-hashed  
- replaced  
- reinterpreted  
- migrated  

The transition applies forward-only.

## 4. Verification

Independent computation of SHA3-384 is possible with standard cryptographic libraries implementing FIPS 202 (e.g., hashlib in Python ≥3.6, OpenSSL, or equivalent tooling).

No proprietary tool is required.

Example computation (Python):

```python
import hashlib

digest = hashlib.sha3_384()
with open("example.md", "rb") as f:
    for chunk in iter(lambda: f.read(8192), b""):
        digest.update(chunk)

print(digest.hexdigest())  # 96 hexadecimal characters (lowercase)
