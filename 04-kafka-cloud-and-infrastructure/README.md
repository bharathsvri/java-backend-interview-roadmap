# Month 4 — Kafka, Cloud, and Infrastructure

> **Timeline:** January 2027  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#january-2027--kafka-cloud-and-infrastructure) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 4 dives into high-throughput distributed event streaming with Apache Kafka, in-memory distributed caching with Redis, enterprise AWS cloud architecture, containerization with multi-stage Dockerfiles, Kubernetes orchestration, and automated CI/CD pipelines.

## 📂 Recommended Directory Structure

```text
04-kafka-cloud-and-infrastructure/
├── notes/                        # Distributed data & infrastructure blueprints
│   ├── kafka-internals.md        # Partitions, consumer rebalancing, EOP, DLQ
│   ├── redis-caching-patterns.md # Cache-aside, stampede defense, Redlock
│   ├── aws-cloud-architecture.md # ECS/EKS, RDS Multi-AZ, S3, IAM, SQS/SNS
│   ├── docker-best-practices.md  # Multi-stage Java builds, minimal base images
│   ├── kubernetes-workloads.md   # Deployments, Services, Ingress, Probes, HPA
│   └── cicd-github-actions.md    # Testcontainers, automated build/test/publish
├── code-examples/                # Infrastructure configurations & scripts
│   ├── kafka-producer-consumer/  # Idempotent producer & transactional listener
│   ├── redis-distributed-lock/   # Redisson distributed locking pattern
│   ├── docker/                   # Optimized Dockerfile for Spring Boot
│   └── k8s-manifests/            # Deployment, Service, ConfigMap, and Ingress
└── dsa-practice/                 # Month 4 DSA problems (Heaps, Tries, Graphs)
```

## 🎯 Key Study Topics

1. **Apache Kafka Event Streaming:**
   - Distributed commit log, partition replication, In-Sync Replicas (ISR).
   - Producer batching (`linger.ms`, `batch.size`), ACKs (`0, 1, all`), idempotent producer.
   - Consumer groups, partition assignment, cooperative rebalancing, offset management.
   - Message delivery semantics (At-most-once, At-least-once, Exactly-once processing).
   - Dead Letter Queues (DLQ), retry topics, Spring Kafka integration.
2. **Redis & Distributed Caching:**
   - In-memory data structures (Strings, Hashes, ZSets, Bitmaps).
   - Caching strategies: Cache-Aside, Write-Through, Write-Behind, Refresh-Ahead.
   - Caching pitfalls: Cache Stampede, Penetration (Bloom Filters), Avalanche (jittered TTLs).
   - Distributed locking with Redisson (watchdog renewal, fair locks, reentrancy).
3. **AWS Cloud Essentials:**
   - Compute: EC2, ECS, EKS.
   - Storage & Database: S3 lifecycle, RDS Multi-AZ, Aurora, DynamoDB single-table design.
   - Networking & Security: VPC, Subnets, NAT Gateways, Security Groups, IAM least privilege.
   - Messaging: SQS FIFO/Standard, SNS fanout.
4. **Docker & Containerization:**
   - Multi-stage Dockerfile design for Java (layer caching, Distroless/Temurin JRE).
   - Docker Compose for local full-stack topologies (App + PostgreSQL + Kafka + Redis).
5. **Kubernetes (K8s) Orchestration:**
   - Pods, Deployments, Services (`ClusterIP`, `LoadBalancer`), Ingress.
   - ConfigMaps, Secrets, Liveness/Readiness/Startup health probes, HPA autoscaling.
6. **CI/CD Pipelines:**
   - Automated testing with GitHub Actions & Testcontainers.
   - Container image build, security scan, and registry publishing.
7. **DSA (Target: 25–30 problems, Cumulative: 100–120):**
   - Heaps / Priority Queues, Tries (Prefix tree), Graphs (BFS, DFS, Cycle Detection, Topological Sort, Dijkstra).

## 🏆 Monthly Milestone
- Implement resilient Kafka producers and consumers with manual offset commits, retry topics, and DLQs.
- Configure Redis distributed caching with stampede prevention and distributed locks using Redisson.
- Containerize a Spring Boot application using multi-stage Docker builds and deploy to Kubernetes.
- Cross the 100-problem milestone in DSA, mastering Heaps, Tries, and Graph traversals.
