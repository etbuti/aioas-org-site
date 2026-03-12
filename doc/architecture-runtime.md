# OAS Runtime Architecture

This diagram shows the **actual running structure** of the Origin Audit Standard system.

Reality
│
▼
Runner (runner_oas_test.py)
│
▼
Proof Package
(manifest.json + artifacts)
│
▼
Anchor Chain
(anchor.log)
│
▼
Verification
(verify_oas.py)
│
▼
Signature Layer
(oas-sign)
│
▼
Node Identity
(node.json)
---

## Components

### Runner

Generates audit reports from observed system state.

Example implementation:

runner_oas_test.py
---

### Proof Package

Deterministic audit report package.

Files:

manifest.json
artifacts/*
The proof hash is recorded in the anchor chain.

---

### Anchor Chain

Append-only hash chain used to anchor proof hashes.

File:

anchor.log
Each entry links to the previous hash to ensure immutability.

---

### Verification

Open deterministic verification algorithm.

Reference implementation:

verify_oas.py
Verification checks:

- manifest self-hash  
- artifact integrity  
- anchor presence  
- anchor chain continuity  

---

### Signature Layer

Optional trust endorsement layer.

Example field:

signatures[]
Signatures extend the trust layer without modifying the proof hash.

---

### Node Identity

Public declaration of a signing node.

File:

node.json
Typical fields:

- node_id
- public_key
- network metadata
- 
