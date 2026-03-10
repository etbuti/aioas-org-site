# OAS vs Blockchain vs PKI vs Logs

```mermaid
flowchart TB

subgraph Observability
A[Logs]
B[Metrics]
C[Events]
end

subgraph OAS
D[Proof Package]
E[Deterministic Verification]
F[Signature Trust]
end

subgraph Blockchain
G[Transactions]
H[Consensus]
I[Distributed Ledger]
end

subgraph PKI
J[Certificate Authority]
K[Identity Trust]
end

A --> D
B --> D
C --> D

D --> E
E --> F

G --> H
H --> I

J --> K
