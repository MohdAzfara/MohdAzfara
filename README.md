<div align="center">

# Hi, I'm  Mohd Azfara  👋

### **Principal Fintech & Distributed Systems Architect**

*Fault-tolerant payment orchestration, multi-PSP failover routing, and zero-trust financial infrastructure.*

[![TypeScript](https://img.shields.io/badge/TypeScript-5.0%2B-blue.svg)](https://www.typescriptlang.org/)
[![SemVer](https://img.shields.io/badge/SemVer-1.0.0-green.svg)](https://semver.org/)
[![RFC 9116](https://img.shields.io/badge/Security-RFC%209116-informational.svg)](.well-known/security.txt)
[![TLA+](https://img.shields.io/badge/Formal%20Verification-TLA%2B-orange.svg)](docs/formal-verification/)

</div>

---

I design and maintain mission-critical payment systems where **idempotency**, **strict auditability**, and **zero-data-loss recovery** are non-negotiable.

---

### 🏛️ Core Engineering Focus

* **Payment Orchestration & Routing:** Multi-PSP failover mechanisms, FSM circuit breakers, deterministic multi-rail payout routing, and secure client-side tokenization SDKs.
* **Formal Verification & Security:** Applying TLA+ mathematical specifications for concurrency safety, STRIDE threat modeling, and zero-trust cryptographic payload attestation.
* **Ledger & Reconciliation Systems:** Two-phase balance reservation, immutable double-entry bookkeeping, automated three-way settlement matching, and balance invariants.
* **Asynchronous Event Pipelines:** Distributed background workers utilizing Redis Streams & BullMQ with Full-Jitter exponential backoff and Dead-Letter Queue (DLQ) isolation.
* **Security & Compliance:** PCI-DSS scope reduction, RFC 9116 security disclosures, ISO 20022 control alignment, HMAC webhook verification, and constant-time signature comparison.

---

### 🛠️ Technical Stack & Tooling

| Domain | Technologies & Standards |
| :--- | :--- |
| **Languages** | TypeScript, Node.js, Go, SQL |
| **Data & State** | PostgreSQL (ACID / Serializable Locking), Redis (Streams & Redlock) |
| **Messaging** | Apache Kafka, RabbitMQ, BullMQ |
| **Infrastructure** | Docker, Kubernetes, AWS (ECS, KMS, SQS), GitHub Actions |
| **Standards & Verification** | RESTful APIs, gRPC, OpenAPI 3.1, TLA+ Formal Specs, ISO 20022 Concepts |

---

### 🚀 Featured Open-Source Architecture

| Project | Architecture Role | Core Stack |
| :--- | :--- | :--- |
| [checkout-flow-sdk](https://github.com/MohdAzfara/checkout-flow-sdk) | Client-side checkout & tokenization SDK with multi-provider failover, TLA+ verification, and STRIDE security models | TypeScript, WebCrypto, TLA+ |
| [payout-gateway-service](https://github.com/MohdAzfara/payout-gateway-service) | High-throughput asynchronous payout microservice with two-phase balance locking and three-way reconciliation | TypeScript, Node.js, PostgreSQL |
| [automated-refund-worker](https://github.com/MohdAzfara/automated-refund-worker) | Event-driven worker for idempotent refund pipelines & fraud audits | TypeScript, Node.js, Redis, BullMQ |
| [double-entry-ledger-core](https://github.com/MohdAzfara/double-entry-ledger-core) | Production-grade immutable double-entry accounting ledger enforcing strict ACID invariants | TypeScript, Node.js, PostgreSQL |

---

### 📐 Architectural Design Principles

1. **Idempotency by Default:** Every state-mutating request requires an `Idempotency-Key`, enforced at both the API boundary and database constraint layer to prevent duplicate ledger debits.
2. **Two-Phase Balance Integrity:** Outbound fund disbursements enforce synchronous available-to-pending balance reservation locks before external banking dispatch.
3. **Event-Driven Decoupling:** Critical payment paths respond synchronously only for authorization; settlement, notifications, and reconciliation audits process asynchronously via durable queues.
4. **Rigorous Formal Verification:** Core business logic, idempotency invariants, and state machine transitions are backed by TLA+ mathematical models to eliminate concurrency anomalies.

---

### 📬 Contact & Security Disclosures

* **Email:** lumilieju@hotmail.com[span_0](start_span)[span_0](end_span)
* **Security Policy:** Adheres to RFC 9116 vulnerability disclosure standards across all managed repositories.
