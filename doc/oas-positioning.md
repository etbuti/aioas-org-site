# OAS Positioning

This diagram explains where the **Origin Audit Standard (OAS)** sits
relative to other common trust systems.

```mermaid
flowchart TB

subgraph Logs["Operational Logs"]
A1[Logs]
A2[Metrics]
A3[Events]
end

subgraph Blockchain["Blockchain Systems"]
B1[Transactions]
B2[Consensus]
B3[Ledger]
end

subgraph PKI["Public Key Infrastructure"]
C1[Certificates]
C2[Certificate Authorities]
end

subgraph OAS["Origin Audit Standard"]
D1[Proof Package]
D2[Verification]
D3[Signatures]
end

Logs --> D1

D1 --> D2
D2 --> D3

PKI --> D3

Blockchain --> D3
