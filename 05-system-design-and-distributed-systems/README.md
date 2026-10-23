# Month 5 — System Design and Distributed Systems

> **Timeline:** Month 5 (Self-Paced / 4 Weeks)  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#month-5--system-design-and-distributed-systems) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 5 focuses on high-level and low-level system design, distributed systems consensus and consistency patterns, resilience engineering, security and compliance, and deep dives into critical FinTech architectural blueprints (Double-Entry Ledgers, Payment Gateways, and Order Matching Engines).

## 📂 Recommended Directory Structure

```text
05-system-design-and-distributed-systems/
├── notes/                           # System design frameworks & pattern guides
│   ├── system-design-framework.md   # Requirements, back-of-the-envelope, deep dive
│   ├── distributed-transactions.md  # 2PC, Saga (Orchestration vs Choreography), Outbox
│   ├── rate-limiting-algorithms.md  # Token Bucket, Leaky Bucket, Sliding Window Log
│   ├── security-and-compliance.md   # mTLS, Zero Trust, PCI-DSS, PII tokenization
│   └── observability.md             # OpenTelemetry, Prometheus, Grafana, ELK
├── case-studies/                    # FinTech & High-Scale Design Blueprints
│   ├── 01-payment-gateway.md        # State machine, idempotency, webhook reconciliation
│   ├── 02-double-entry-ledger.md    # Immutable ledger, debit/credit invariant, audit trail
│   ├── 03-digital-wallet.md         # Balance locking, low latency, hot/cold reserves
│   ├── 04-order-matching-engine.md  # CLOB, LMAX Disruptor, price-time priority
│   └── 05-distributed-rate-limiter.md # Redis + Lua script implementation
└── dsa-practice/                    # Month 5 DSA problems (DP, Backtracking, Greedy)
```

## 🎯 Key Study Topics

1. **System Design Fundamentals & Framework:**
   - 4-step interview template: Clarify scope -> Back-of-the-envelope -> High-Level Design -> Deep Dive.
   - CAP Theorem & PACELC Theorem trade-offs.
   - Scalability: Horizontal vs. Vertical, stateless compute, database sharding & read replicas.
   - High Availability: Multi-region active-active/active-passive, RPO and RTO.
   - Load balancing (Layer 4 vs. Layer 7), Consistent Hashing with virtual nodes.
2. **Distributed Systems Communication & Patterns:**
   - Communication protocols: REST, gRPC (HTTP/2, Protobuf), WebSockets, Message Queues.
   - Idempotency key design and deduplication mechanisms.
   - Distributed transactions: Two-Phase Commit (2PC) bottlenecks.
   - Saga Pattern (Choreography vs. Orchestration) with compensating actions.
   - Transactional Outbox Pattern with Change Data Capture (CDC / Debezium).
   - Event Sourcing & CQRS architectures.
3. **Resilience & Fault Tolerance:**
   - Rate Limiting algorithms: Token Bucket, Leaky Bucket, Sliding Window Counter.
   - Circuit Breakers (states, thresholds), Bulkheads, Retries with exponential backoff & full jitter.
4. **FinTech System Design Deep Dives:**
   - **Payment Gateway:** Idempotent payment API, state machine, webhook verification, reconciliation.
   - **Double-Entry Ledger:** Immutable accounting ledger, debit/credit balance invariance ($Assets = Liabilities + Equity$).
   - **Digital Wallet:** Fast balance mutations, avoiding row lock contention, reserve accounts.
   - **High-Throughput Order Matching Engine:** Central Limit Order Book (CLOB), LMAX Disruptor, deterministic replay.
   - **Fraud Detection:** Real-time event streaming, rule engines, velocity checks.
5. **Security, Observability & Compliance:**
   - Zero Trust, mTLS between services, HashiCorp Vault secrets management.
   - PCI-DSS requirements, PII encryption and masking.
   - Distributed Tracing (W3C TraceContext), Prometheus metrics, Grafana dashboards, ELK logging.
6. **DSA (Target: 25–30 problems, Cumulative: 125–150):**
   - Dynamic Programming (1D/2D DP, 0/1 Knapsack, LCS, LIS), Backtracking, Greedy Algorithms.

## 🏆 Monthly Milestone
- Confidently lead a 45-minute System Design interview, providing clear architecture diagrams and trade-off rationales.
- Defend the implementation of distributed consistency patterns: Sagas, Outbox, and Event Sourcing.
- Articulate the architecture of a production Payment Gateway and a Double-Entry Bookkeeping Ledger.
- Reach 125–150 solved quality DSA problems, mastering Dynamic Programming and Backtracking.
