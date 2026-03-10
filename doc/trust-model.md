# trust-model

```mermaid
flowchart LR

Reality --> Proof

Proof --> Verification

Verification --> SignA["Node A Signature"]
Verification --> SignB["Node B Signature"]
Verification --> SignC["Node C Signature"]

SignA --> Trust
SignB --> Trust
SignC --> Trust

Trust["Growing Trust Layer
(append-only)"]
