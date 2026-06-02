# Hi, I'm Dmitry Karpenko 👋
### Senior .NET Developer & Systems Engineer

I am a backend and systems-oriented engineer focused on building high-performance data processing pipelines, network protocol analyzers, and infrastructure-level applications. 

I approach architecture from a systems perspective: focusing on data flow, memory efficiency (zero-allocation), and robust deployment models, bridging the gap between enterprise logic, cloud infrastructure, and hardware telemetry.

---

### 🧠 Core Engineering Philosophy
> **Ingestion → Processing (Backpressure) → Normalization → Output**
> *Designing systems that handle real-world telemetry and network streams reliably.*

---

### 🏗️ My Engineering Ecosystem

This is the architectural layered model I use to build and scale systems, from low-level network packets to high-level enterprise workflows.

```mermaid
flowchart TD
    classDef layer fill:#0d1117,stroke:#30363d,stroke-width:2px,color:#c9d1d9,rx:8px,ry:8px;
    classDef tech fill:#161b22,stroke:#21262d,stroke-width:1px,color:#58a6ff;

    subgraph Business["🏢 Business Layer (Enterprise & Workflow)"]
        direction TB
        M["Healthcare & Patient Management (MedCert)"]:::tech
        Stack1["ASP.NET Core • Clean Architecture • Dapper • Redis"]:::tech
        M --- Stack1
    end
    class Business layer

    subgraph Infra["🐳 Infrastructure Layer (Deployment & Routing)"]
        direction TB
        T["Multi-Tenant Isolation Platform"]:::tech
        Stack2["Docker • Traefik Reverse Proxy • Cloud Ready"]:::tech
        T --- Stack2
    end
    class Infra layer

    subgraph Observability["📊 Observability Layer (Telemetry & Backpressure)"]
        direction TB
        L["LogPulse Aggregation Pipeline"]:::tech
        Stack3["Syslog / Winlogbeat • Bounded Channels • Resilient Streaming"]:::tech
        L --- Stack3
    end
    class Observability layer

    subgraph Network["📡 Network Layer (Low-level Data Processing)"]
        direction TB
        N["NetDissector / Packet Analysis"]:::tech
        Stack4["Ethernet -> IP -> TCP • System.IO.Pipelines • Zero-Allocation"]:::tech
        N --- Stack4
    end
    class Network layer

    Business -->|Containerized Services| Infra
    Infra -->|Logs & Metrics| Observability
    Observability -->|Traffic Analysis| Network
```

### 🚀 Technical Arsenal
* **Backend & Architecture**: .NET, C#, Clean Architecture, REST APIs, Dapper

* **Systems & Performance**: `System.IO.Pipelines`, Bounded Channels (Backpressure), `ReadOnlySpan`, Zero-Allocation Parsing

* **Networking**: Packet Analysis (Ethernet/IP/TCP), NetFlow v9, MikroTik Routing, Protocol Decoders

* **Infrastructure & OS**: Docker, Traefik, Debian Linux, Redis, Syslog

* **Currently Preparing For**: AWS Certified Developer (DVA-C02)

### 💡 Featured Projects
* **NetDissector**: A low-level network packet parsing engine built with C#. Highly optimized for high-throughput traffic using struct-based parsing and `System.IO.Pipelines` to minimize memory allocations.

* **LogPulse**: A backpressure-aware telemetry collector. Designed to safely ingest traffic spikes from hardware routers (MikroTik Syslog) and Windows environments without throwing OOM exceptions.

* **MedCert Platform**: A workflow-driven patient management system utilizing strict state validation and domain-driven design principles for immutable auditability.
