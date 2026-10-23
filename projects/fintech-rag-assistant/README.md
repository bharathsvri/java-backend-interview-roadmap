# Project: FinTech RAG Assistant

> **Module:** [Month 6 — Generative AI and RAG](../../06-generative-ai-and-rag/README.md)  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../../6-Month-Interview-Roadmap.md#month-6--generative-ai-and-rag)

---

## 📌 Project Overview

The **FinTech RAG Assistant** is a production-grade document intelligence platform built with Java, Spring Boot, Spring AI, and PostgreSQL `pgvector`. It parses complex financial filings, performs semantic vector search with HNSW indexes, and streams verifiable answers with citations and PII protection.

## 🏗️ Architecture Blueprint

```text
User / Frontend
      │ (SSE Stream)
      ▼
Spring Boot 3 Web Application (Spring WebFlux / MVC)
      │
      ├──> Spring Security (JWT Authentication & RBAC)
      ├──> Input Guardrail (Prompt Injection Sanitizer & PII Masking)
      │
      ├──> Hybrid Retrieval Engine
      │         ├──> PostgreSQL (pgvector HNSW Dense Cosine Similarity)
      │         └──> Full-Text Search (Sparse BM25 Index)
      │                     │
      │                     ▼ (Reciprocal Rank Fusion - RRF)
      │               Re-ranking / Candidate Chunk Selection
      │
      ├──> Spring AI ChatClient (Tool Calling & Prompt Synthesis)
      │         └──> External LLM (OpenAI / Claude / Local Ollama)
      │
      └──> PostgreSQL Audit Log (Queries, Retrieved Chunks, Prompt History)
```

## 🛠️ Tech Stack
- **Framework:** Spring Boot 3+, Spring AI
- **Database:** PostgreSQL 16+ with `pgvector`
- **Security:** Spring Security (Stateless JWT)
- **Streaming:** Server-Sent Events (SSE)
- **Containerization:** Docker & Docker Compose
