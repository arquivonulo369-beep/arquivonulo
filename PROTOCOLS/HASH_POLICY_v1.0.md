# ARQUIVONULO GLOBAL
## HASH POLICY PROTOCOL
Version: 1.0
Status: Active
Adoption Date: 2026-02-20
Classification: Protocol
Canonical Algorithm: SHA3-384

---

## 1. Purpose

This protocol defines the cryptographic integrity framework of ArquivoNulo Global.

Its function is not security hardening.
Its function is deterministic integrity governance.

---

## 2. Canonical Algorithm

The exclusive canonical hashing algorithm is:

SHA3-384

No alternative algorithm is considered authoritative for state validation.

---

## 3. Sealing Requirement

The following categories require canonical sealing:

- STATE files
- MANIFESTO files
- Governance policies
- Institutional declarations
- Any file explicitly marked as canonical

Each sealed document must have a sidecar file:

<filename>.sha3-384

The sidecar must contain only the hexadecimal digest.

---

## 4. Verification Procedure

Command:

openssl dgst -sha3-384 <filename>

The resulting digest must exactly match the content of:

<filename>.sha3-384

Any mismatch invalidates the canonical state.

---

## 5. Forward-Only Integrity Model

ArquivoNulo Global operates under:

- No destructive edits of sealed documents.
- No history rewriting.
- No canonical mutation.

If modification is required:

1. Create a new versioned document.
2. Generate a new SHA3-384 seal.
3. Preserve historical continuity.

Integrity is cumulative.

---

## 6. Constitutional Binding

This protocol is binding to all canonical layers of the system.

Deviation requires:

- Explicit documentation
- Version increment
- New canonical state freeze

---

END OF HASH_POLICY_v1.0
