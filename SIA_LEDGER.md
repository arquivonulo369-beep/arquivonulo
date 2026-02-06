# ArquivoNulo — SIA Ledger (Proof of Issuance)

CANON REFERENCE: 2026-02-06T10:00:00Z

---

## 1. Purpose

This ledger serves as a public registry of cryptographic hashes for all issued
Standing Invocation Acknowledgments (SIA).

It provides verifiable proof of existence and issuance date without disclosing
confidential entity data or the content of the acknowledgments.

---

## 2. Structure

Each entry consists of:
- SIA_ID: A unique institutional identifier.
- SHA-256 HASH: The cryptographic fingerprint of the issued PDF.
- TIMESTAMP: Date and time of issuance (UTC).

---

## 3. Registry

| SIA_ID | SHA-256 HASH (SIA PDF) | TIMESTAMP (UTC) |
| :--- | :--- | :--- |
| SIA-INIT-2026-000 | 0000000000000000000000000000000000000000000000000000000000000000 | 2026-02-06T10:00:00Z |

---

## 4. Verification

To verify an acknowledgment, calculate the SHA-256 hash of the SIA PDF document
provided by the entity and compare it with the hash recorded in this ledger.
Any mismatch indicates a non-canonical or tampered document.

---
End of Ledger.
