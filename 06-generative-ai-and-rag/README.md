# Month 6 — Generative AI and RAG

> **Timeline:** March 2027  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#march-2027--generative-ai-and-rag) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 6 explores the modern Generative AI engineering stack: Large Language Model fundamentals, vector embeddings, high-dimensional vector search with PostgreSQL `pgvector`, production Retrieval-Augmented Generation (RAG) pipelines, Spring AI framework integration, AI security guardrails, and building the domain-specific **FinTech RAG Assistant**.

## 📂 Recommended Directory Structure

```text
06-generative-ai-and-rag/
├── notes/                        # GenAI architectures & retrieval mechanics
│   ├── llm-transformers.md       # Self-attention, tokenization, hyperparameters
│   ├── vector-databases.md       # Dense vectors, cosine similarity, HNSW vs IVFFlat
│   ├── rag-pipeline-patterns.md  # Chunking, hybrid search (BM25 + vector), re-ranking
│   ├── spring-ai-internals.md    # ChatClient, PromptTemplate, VectorStore, Tool Calling
│   └── ai-security-guardrails.md # Prompt injection, PII masking, Ragas evaluation
├── code-examples/                # Hands-on GenAI code
│   ├── pgvector-demo/            # Schema setup, HNSW indexing, similarity queries
│   ├── spring-ai-tools/          # Function Calling / Tool Calling in Spring AI
│   └── streaming-chat/           # SSE streaming responses with Spring WebFlux
├── project/                      # Hands-on Project: FinTech RAG Assistant
│   └── (See projects/fintech-rag-assistant/)
└── dsa-practice/                 # Month 6 DSA problems (Advanced Graphs, Hard DP, Revisions)
```

## 🎯 Key Study Topics

1. **LLM Fundamentals & Architectures:**
   - Transformer architecture, Self-Attention mechanism, tokenization (BPE), context windows.
   - Hyperparameters: Temperature, Top-P (nucleus sampling), Top-K, Frequency/Presence penalty.
   - Prompt engineering: Few-shot, Chain-of-Thought (CoT), ReAct prompting.
2. **Vector Embeddings & Vector Databases:**
   - Text embeddings and semantic similarity metrics (Cosine similarity, Dot Product, Euclidean distance).
   - PostgreSQL with `pgvector`: vector column types, `<=>` (cosine distance) operator.
   - Vector indexing algorithms: Approximate Nearest Neighbor (ANN), IVFFlat vs. HNSW graphs (`m`, `ef_construction`).
3. **Retrieval-Augmented Generation (RAG) Architecture:**
   - Ingestion: Document parsing (PDF statements, SEC filings), chunking strategies (semantic, recursive, overlap).
   - Retrieval: Dense vector retrieval, Sparse keyword search (BM25), Hybrid search (Reciprocal Rank Fusion - RRF).
   - Re-ranking (cross-encoders, Cohere Rerank) and citation synthesis.
4. **Spring AI & Java GenAI Ecosystem:**
   - Spring AI abstractions: `ChatClient`, `ChatModel`, `Prompt`, `EmbeddingModel`, `VectorStore` (`PgVectorStore`).
   - Function Calling / Tool Calling: binding Java methods (`java.util.function.Function`) to LLM tool invocations.
5. **AI Security, Guardrails & Evaluation:**
   - Prompt injection defense (direct & indirect), jailbreak prevention.
   - PII masking and data sanitization for compliance.
   - Evaluation frameworks: Ragas (Faithfulness, Answer Relevance, Context Precision, Context Recall).
6. **Hands-on Project: FinTech RAG Assistant:**
   - Financial document query assistant using Spring Boot, Spring AI, PostgreSQL `pgvector`, streaming SSE, and full audit logging.
7. **DSA (Target: 20–25 problems, Cumulative: 150–175):**
   - High-difficulty problems, advanced graph variations, string pattern algorithms (KMP, Trie), timed mock screens.

## 🏆 Monthly Milestone
- Build and evaluate a complete RAG pipeline with hybrid search and document re-ranking.
- Implement LLM Function Calling in Java using Spring AI to allow language models to query backend databases.
- Ship the **FinTech RAG Assistant** with streaming responses and strict source citations.
- Reach 150+ solved quality DSA problems under interview time constraints.
