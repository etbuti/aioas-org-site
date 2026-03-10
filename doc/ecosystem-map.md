# AI Origins Ecosystem Map

```mermaid
flowchart TB

subgraph Identity["Identity Root"]
A[evanbei.com<br>identity / origin root]
end

subgraph Lab["Research & Experiment Layer"]
B[aiorigins.org<br>lab / experiments / audit R&D]
end

subgraph Explanation["Explanation Layer"]
C[aipoints.org<br>explanation / diagrams / public interpretation]
end

subgraph Protocol["Protocol Layer"]
D[aioas.org<br>OAS protocol root]
E[spec<br>report standard / verification / signatures]
F[reference implementation<br>verifier / tools / examples]
end

subgraph Trust["Trust Runtime Layer"]
G[Runner]
H[Proof Package]
I[Anchor Chain]
J[Verification]
K[Signature Layer]
L[Node Identity]
end

subgraph Governance["Governance / Authorization Layer"]
M[aioas.uk<br>governance / authorization / future licensing]
N[aioa.uk<br>future association]
O[aioe.uk<br>future ecosystem]
end

A --> B
A --> C
A --> D

B --> D
C --> D

D --> E
D --> F

F --> G
G --> H
H --> I
H --> J
I --> J
J --> K
K --> L

D --> M
M --> N
M --> O
