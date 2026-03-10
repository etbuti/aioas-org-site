# OAS Core Protocol Architecture

```mermaid
flowchart TB

Reality["Reality / Observed System"]

Runner["Audit Runner"]

Proof["Proof Package
manifest.json
artifacts/*"]

Anchor["Anchor Chain
anchor.log"]

Verify["Deterministic Verification
verify_oas.py"]

Signature["Signature Layer
signatures[]"]

Trust["Trust Accumulation"]

Node["Node Identity
node.json"]

Reality --> Runner

Runner --> Proof

Proof --> Anchor

Proof --> Verify
Anchor --> Verify

Verify --> Signature

Signature --> Trust

Trust --> Node
