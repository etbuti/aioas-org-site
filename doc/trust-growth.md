# OAS Trust Growth Model

```mermaid
flowchart LR

subgraph Phase1["Phase 1 · Single Node Proof"]
A1[Single Runner]
A2[Proof Package]
A3[Anchor Chain]
A4[Single Signature]
end

subgraph Phase2["Phase 2 · Verified Trust"]
B1[Independent Verifier]
B2[Verified Proof]
B3[Append-Only Signature]
end

subgraph Phase3["Phase 3 · Multi-Signature Trust"]
C1[Node A Signature]
C2[Node B Signature]
C3[Node C Signature]
C4[Shared Proof]
end

subgraph Phase4["Phase 4 · Trust Network"]
D1[Multiple Signed Proofs]
D2[Inter-Node Endorsement]
D3[Trust Graph]
end

A1 --> A2
A2 --> A3
A3 --> A4

A2 --> B1
A3 --> B1
B1 --> B2
B2 --> B3

B2 --> C4
C4 --> C1
C4 --> C2
C4 --> C3

C1 --> D1
C2 --> D1
C3 --> D1

D1 --> D2
D2 --> D3
