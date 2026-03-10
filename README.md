# AI Origins / AIPoints / OAS

```mermaid
flowchart TB

subgraph Ecosystem
AIOrigins["AI Origins
Network Layer"]
AIPoints["AI Points
Entry & Node Registry"]
end

subgraph Protocol
OAS["Origin Audit Standard (OAS)
Deterministic Audit Protocol"]
end

subgraph Runtime
Runner["Runner
Audit Generator"]

Proof["Proof Package
manifest.json
artifacts"]

Anchor["Anchor Chain
anchor.log"]

Verify["Independent Verification
verify_oas.py"]

Sign["Signature Layer
append-only signatures"]
end

AIOrigins --> AIPoints
AIPoints --> OAS

OAS --> Runner
Runner --> Proof
Proof --> Anchor

Proof --> Verify
Anchor --> Verify

Verify --> Sign
