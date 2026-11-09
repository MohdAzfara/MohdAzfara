<div align="center">

# **HI, I'M MOHD AZFARA** 👋

### **Principal Fintech & Distributed Systems Architect**

*Architecting fault-tolerant payment orchestration, immutable double-entry ledgers, multi-rail settlement engines, and zero-trust financial infrastructure.*

[![TypeScript](https://img.shields.io/badge/TypeScript-5.0%2B%20(100%25)-blue.svg)](https://www.typescriptlang.org/)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1.0-6ba539.svg)](https://github.com/MohdAzfara?tab=repositories)
[![Formal Verification](https://img.shields.io/badge/Formal_Verification-TLA%2B_(12_Specs)-orange.svg)](https://github.com/MohdAzfara?tab=repositories)
[![Compliance](https://img.shields.io/badge/Compliance-PCI--DSS_v4.0_%7C_ISO_20022-007ec6.svg)](https://github.com/MohdAzfara?tab=repositories)
[![Security](https://img.shields.io/badge/Security-RFC_9116-informational.svg)](https://github.com/MohdAzfara?tab=repositories)

</div>

---

I design and maintain mission-critical financial infrastructure where **idempotency**, **zero-sum mathematical conservation**, **cryptographic auditability**, and **zero-data-loss recovery** are non-negotiable.

---

### 🗺️ End-to-End Financial Ecosystem Architecture

```text
         ┌────────────────────────────────────────────────┐
         │               checkout-flow-sdk                │
         │   (Client Tokenization, EMV 3DS2 & Failover)   │
         └───────────────────────┬────────────────────────┘
                                 │ 1. Signed BigInt Capture
                                 ▼
         ┌────────────────────────────────────────────────┐
         │           double-entry-ledger-core             │
         │  (Immutable Zero-Sum Journal & Merkle Chain)   │
         └───────────┬────────────────────────┬───────────┘
                     │                        │
   2a. Two-Phase Lock│                        │2b. Contra-Journal
       & Settlement  ▼                        ▼    & Split Clawback
┌─────────────────────────────┐      ┌─────────────────────────────┐
│   payout-gateway-service    │◄────►│   automated-refund-worker   │
│ (Multi-Rail & 3-Way Match)  │      │ (Cap Guard & Refund Saga)   │
└─────────────────────────────┘      └─────────────────────────────┘
```

---

### 🏛️ Core Engineering Focus

* **Inbound Payment Orchestration & Tokenization (`checkout-flow-sdk`):** Client-side PCI-DSS v4.0 scope reduction, EMV 3-D Secure 2.2 (`3DS2`) Strong Customer Authentication guards, deterministic FSM circuit breakers (`CLOSED` / `OPEN` / `HALF_OPEN`), and latency-aware multi-PSP failover routing.
* **Immutable Double-Entry Accounting (`double-entry-ledger-core`):** Strict 64-bit `BigInt` zero-sum conservation ($\sum \text{Debits} = \sum \text{Credits}$), append-only contra-entry journals, sequential cryptographic hash chaining (`prevHash` $\rightarrow$ `entryHash`), binary Merkle root sealing, deadlock-free Optimistic Concurrency Control (OCC), and multi-currency FX clearing.
* **Outbound Disbursement & Reconciliation (`payout-gateway-service`):** Synchronous two-phase balance reservation (`available` $\rightarrow$ `pending`) eliminating TOCTOU overdrafts, deterministic multi-rail routing (`INSTANT_RTP`, `SEPA_CREDIT`, `ACH_SAME_DAY`, `SWIFT_WIRE`), and automated three-way reconciliation against ISO 20022 `camt.053` bank statements.
* **Compensating Refund Sagas & Fraud Auditing (`automated-refund-worker`):** Atomic cumulative partial refund cap enforcement ($\sum \text{Refunds} \le \text{Captured}$), pre-dispatch 24h fraud velocity scoring, pro-rata connected vendor balance clawbacks, and fencing-token distributed sagas with Dead-Letter Queue (DLQ) isolation.
* **Formal Verification & Regulatory Rigor:** Every repository is standardized with **6 Architecture Decision Records (24 ADRs total)**, **3 TLA+ formal specifications (12 mathematical models total)**, **OpenAPI 3.1 contracts**, **STRIDE threat models**, **RFC 9116 disclosures**, and **5 deterministic micro-benchmarks (20 suites total)**.

---

### 🛠️ Technical Stack & Tooling

| Domain | Technologies & Standards |
| :--- | :--- |
| **Languages & Runtime** | TypeScript 5.0+ (100% Pure Type-Safe Codebases), Node.js 20.18.0 LTS, Go, SQL |
| **Data, Ledger & State** | PostgreSQL (Serializable ACID / Optimistic CAS Locking), Redis (Streams & Redlock), 64-Bit `BigInt` Minor Units |
| **Messaging & Workers** | Apache Kafka, RabbitMQ, BullMQ, AWS-Style Full-Jitter Exponential Backoff & DLQ Pipelines |
| **Infrastructure & CI/CD** | Docker, Kubernetes, AWS (ECS, KMS, SQS), GitHub Actions, Deterministic `package-lock.json` Supply-Chain Guards |
| **Standards & Verification** | TLA+ Formal Verification, OpenAPI 3.1.0, ISO 20022 (`pain.001`, `pacs.004`, `camt.053`), PCI-DSS v4.0, EMV 3DS 2.2, SOC 1 Type II, GAAP/IFRS, W3C `traceparent`, RFC 9116 |

---

### 🚀 Featured Open-Source Architecture

| Project | Architecture Role & Financial Invariants | Core Stack & Verification |
| :--- | :--- | :--- |
| [**checkout-flow-sdk**](https://github.com/MohdAzfara/checkout-flow-sdk) | Zero-trust client checkout SDK featuring PAN tokenization, EMV 3DS 2.2 cryptogram attestation, latency-weighted multi-PSP failover, FSM circuit breakers, and `BigInt` capture journal emission | TypeScript, WebCrypto, TLA+ (3 Specs), OpenAPI 3.1, PCI-DSS v4.0 |
| [**payout-gateway-service**](https://github.com/MohdAzfara/payout-gateway-service) | High-throughput asynchronous vendor payout microservice enforcing two-phase ACID balance locking, multi-rail failover (`RTP`/`SEPA`/`ACH`/`SWIFT`), and ISO 20022 `camt.053` three-way reconciliation | TypeScript, Node.js, PostgreSQL, TLA+ (3 Specs), OpenAPI 3.1 |
| [**automated-refund-worker**](https://github.com/MohdAzfara/automated-refund-worker) | Event-driven background worker enforcing cumulative partial refund caps, pre-dispatch fraud velocity auditing, pro-rata vendor payout clawbacks, and compensating distributed sagas (`pacs.004`) | TypeScript, Node.js, Redis, BullMQ, TLA+ (3 Specs), OpenAPI 3.1 |
| [**double-entry-ledger-core**](https://github.com/MohdAzfara/double-entry-ledger-core) | Production-grade immutable double-entry accounting engine enforcing strict $\sum \text{Debits} = \sum \text{Credits}$ conservation, hash-chained audit trails, Merkle root sealing, OCC locking, and EOD Trial Balances | TypeScript, Node.js, PostgreSQL, TLA+ (3 Specs), SOC 1 / GAAP |

---

### 📐 Architectural Design Principles

1. **Idempotency & Payload Attestation by Default:** Every state-mutating request across checkout, payout, refund, and ledger boundaries requires a deterministic `Idempotency-Key` bound to a canonical cryptographic payload fingerprint to eliminate duplicate financial execution.
2. **Strict Zero-Sum & Two-Phase Balance Integrity:** Monetary values are processed exclusively in 64-bit `BigInt` minor units. Outbound payouts and partial refunds enforce synchronous balance/cap reservations prior to external banking dispatch, backed by append-only double-entry journal batches ($\sum \text{Debits} = \sum \text{Credits}$).
3. **Graceful Degradation & Compensating Sagas:** External gateway brownouts trigger deterministic FSM circuit breakers, multi-rail failover routing, or Dead-Letter Queue (DLQ) quarantine with AWS-style Full-Jitter exponential backoff—never premature balance rollbacks.
4. **Mathematical Formal Verification & Tamper Evidence:** Critical concurrency locks, conservation laws, and state machines are proven via **TLA+ specifications** and sealed into sequential cryptographic hash chains and binary Merkle trees.

---

### 📬 Contact & Security Disclosures

* **Email:** [lumilieju@hotmail.com](mailto:lumilieju@hotmail.com)
* **Security Policy:** Adheres strictly to **RFC 9116** (`.well-known/security.txt`) vulnerability disclosure standards and **STRIDE** threat modeling across all managed repositories.
