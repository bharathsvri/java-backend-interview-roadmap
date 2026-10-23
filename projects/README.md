# Portfolio Projects Hub

> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md) | [Repository README](../README.md)

This directory houses the flagship production-grade engineering projects designed to showcase senior-level backend, distributed systems, and Generative AI competencies in technical interviews.

---

## 🚀 Projects Overview

| Project | Month | Focus Domains | Tech Stack | Status |
| :--- | :---: | :--- | :--- | :---: |
| **[FinTech RAG Assistant](./fintech-rag-assistant/)** | Month 6 (March 2027) | Document Intelligence, Regulatory Compliance, Vector Search | Spring Boot 3, Spring AI, PostgreSQL `pgvector`, Spring WebFlux (SSE), Docker | ⏳ Planned |
| **[FinBank + GenAI Platform](./finbank-genai-platform/)** | Month 7 (April 2027) | Core Banking, Double-Entry Ledger, Event Streaming, MCP, Autonomous Agents | Spring Boot 3, Apache Kafka, Redis, PostgreSQL, Spring AI, Model Context Protocol (MCP), Kubernetes | ⏳ Planned |

---

## 1. FinTech RAG Assistant (Month 6)

### Objective
A domain-specific financial document intelligence assistant that parses complex financial statements (SEC filings, quarterly earnings, balance sheets, regulatory circulars) and provides streamed, cited answers with strict compliance guardrails.

### Key Capabilities
- **Hybrid Search Engine:** Combines dense semantic vector retrieval via `pgvector` (HNSW indexing) with BM25 keyword matching using Reciprocal Rank Fusion (RRF).
- **Spring AI Integration:** Implements Spring AI `ChatClient` with custom `@Bean` tool calling for real-time calculation and currency conversion.
- **Safety & Compliance:** Input sanitization to defend against prompt injection and automated PII masking before embedding/prompt dispatch.
- **Full Observability:** PostgreSQL audit log capturing incoming questions, retrieved chunk IDs, similarity scores, and LLM token usage.

---

## 2. FinBank + GenAI Platform (Month 7 Capstone)

### Objective
A comprehensive, end-to-end distributed microservices banking platform coupled with an autonomous GenAI financial analyst agent capable of executing authorized transactions and providing wealth management insights.

### Architecture Highlights
- **Double-Entry Bookkeeping Ledger:** Strict mathematical invariance ($Debit = Credit$) ensuring immutable, tamper-evident financial accounting.
- **High Concurrency & Event Streaming:** Apache Kafka topics for transaction events and fraud detection; Redis for balance caching and distributed locks.
- **Model Context Protocol (MCP) Server:** Custom Java MCP server exposing banking operations (Account Inquiry, Transfer Funds, Generate Statement) as standardized tools to LLMs.
- **Human-in-the-Loop (HITL) Governance:** Strict one-time cryptographic approval tokens required for any balance-mutating tool execution.
- **Production Infrastructure:** Docker Compose and Kubernetes manifests, GitHub Actions CI/CD pipeline, Prometheus + Grafana metrics, and OpenTelemetry tracing.
