### Hi, I'm Mohd Azfar 👋

**Fintech & Distributed Systems Engineer** specializing in fault-tolerant payment orchestration, double-entry ledger architectures, and high-throughput asynchronous workers.

I design and maintain backend financial infrastructure where **idempotency**, **strict auditability**, and **zero-data-loss recovery** are non-negotiable.

---

### 🏗️ Core Engineering Focus

* **Payment Orchestration & Routing:** Multi-PSP failover mechanisms, smart retry strategies, and client-side tokenization SDKs.
* **Ledger & Reconciliation Systems:** Immutable double-entry bookkeeping, automated settlement matching, and discrepancy alerting.
* **Asynchronous Event Pipelines:** Distributed background workers utilizing Redis Streams & message queues for webhook ingestion, fraud scoring, and automated refunds.
* **Security & Compliance:** PCI-DSS scope reduction, HMAC webhook verification, rate-limiting, and cryptographic payload signing.

---

### 🛠️ Technical Stack & Tooling

| Domain | Technologies & Standards |
| :--- | :--- |
| **Languages** | `TypeScript` `Node.js` `Go` `SQL` |
| **Data & State** | `PostgreSQL (ACID / Serializable Locking)` `Redis (Streams & Redlock)` |
| **Messaging** | `Apache Kafka` `RabbitMQ` `BullMQ` |
| **Infrastructure** | `Docker` `Kubernetes` `AWS (ECS, KMS, SQS)` `GitHub Actions` |
| **Standards** | `RESTful APIs` `gRPC` `OpenAPI 3.1` `ISO 20022 Concepts` `Webhook Signatures` |

---

### 📌 Featured Open-Source Architecture

| Project | Architecture Role | Core Stack |
| :--- | :--- | :--- |
| **[checkout-flow-sdk](https://github.com/MohdAzfara/checkout-flow-sdk)** | Client-side checkout & tokenization SDK with multi-provider fallback | `TypeScript` `Rollup` `WebCrypto` |
| **[payout-gateway-service](https://github.com/MohdAzfara/payout-gateway-service)** | High-throughput vendor payout engine & balance reconciliation API | `TypeScript` `Node.js` `PostgreSQL` |
| **[automated-refund-worker](https://github.com/MohdAzfara/automated-refund-worker)** | Event-driven worker for idempotent refund pipelines & fraud audits | `Node.js` `Redis` `BullMQ` |

---

### 📐 Architectural Design Principles

1. **Idempotency by Default:** Every state-mutating request requires an `Idempotency-Key` enforced at the database constraint and distributed lock layer.
2. **Event-Driven Decoupling:** Critical payment paths respond synchronously only for authorization; settlement, notifications, and audit logs are processed asynchronously via durable queues.
3. **Graceful Degradation:** External gateway timeouts trigger circuit breakers and automatic fallback routing rather than cascading system failures.

---

📫 **Contact & Security Disclosures:** [lumillieju@hotmail.com](mailto:lumillieju@hotmail.com)
