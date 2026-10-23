# Capstone Project: FinBank + GenAI Platform

> **Module:** [Month 7 — MCP, Agents, and Final Revision](../../07-mcp-agents-and-final-revision/README.md)  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../../6-Month-Interview-Roadmap.md#april-2027--mcp-agents-and-final-revision)

---

## 📌 Project Overview

**FinBank + GenAI** is a flagship enterprise platform combining distributed core banking microservices with an autonomous Generative AI Financial Analyst Agent powered by Spring AI and the Model Context Protocol (MCP).

## 🏗️ Architecture Blueprint

```text
                               +----------------------------+
                               |     Client Application     |
                               +--------------+-------------+
                                              |
                                              ▼
                             +--------------------------------+
                             |   Spring Cloud API Gateway     |
                             +---------------+----------------+
                                             |
             +-------------------------------+-------------------------------+
             |                               |                               |
             ▼                               ▼                               ▼
+--------------------------+   +--------------------------+   +--------------------------+
|     Account Service      |   |  Transaction & Ledger    |   |     GenAI Agent & MCP    |
| (Spring Boot + Postgres) |   | (Double-Entry Accounting)|   | (Spring AI + Custom MCP) |
+------------+-------------+   +-------------+------------+   +-------------+------------+
             |                               |                              |
             +---------------+---------------+                              |
                             | (Transaction Events)                         | (Tools / Queries)
                             ▼                                              ▼
                 +-----------------------+                    +--------------------------+
                 |     Apache Kafka      |<-------------------|  Autonomous ReAct Agent  |
                 | (Event Streaming Log) |                    | (Tool Calls + HITL Token)|
                 +-----------+-----------+                    +--------------------------+
                             |
                             ▼
                 +-----------------------+
                 |  Fraud Detection Svc  |
                 +-----------------------+
```

## 🛠️ Tech Stack
- **Core Microservices:** Java 21, Spring Boot 3+, Spring Data JPA, Hibernate
- **Database & Cache:** PostgreSQL (Double-Entry Ledger, balance invariance), Redis (caching & distributed locks)
- **Event Streaming:** Apache Kafka (transaction events, audit logging, fraud events)
- **Generative AI & Agentic:** Spring AI, Model Context Protocol (MCP) Java Server, Tool Calling, ReAct Loop
- **Security & Governance:** JWT, Role-Based Access Control, Human-in-the-Loop (HITL) authorization tokens
- **DevOps & Monitoring:** Docker Compose, Kubernetes, GitHub Actions CI/CD, Prometheus, Grafana, OpenTelemetry
