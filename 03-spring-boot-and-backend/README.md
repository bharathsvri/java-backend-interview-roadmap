# Month 3 — Spring Boot and Backend Development

> **Timeline:** December 2026  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#december-2026--spring-boot-and-backend-development) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 3 covers the enterprise Java backend stack: Spring Core IoC container, Spring Boot auto-configuration internals, REST API best practices, Spring Security with stateless JWT and OAuth2, Spring Data JPA/Hibernate tuning, transactional boundary management, PostgreSQL indexing, and microservices architecture.

## 📂 Recommended Directory Structure

```text
03-spring-boot-and-backend/
├── notes/                        # Framework mechanics & database internals
│   ├── spring-ioc-lifecycle.md   # Bean lifecycle, BeanPostProcessor, scopes
│   ├── spring-security-jwt.md    # SecurityFilterChain, token validation, RBAC
│   ├── jpa-hibernate-tuning.md   # Entity mapping, N+1 problem, L1/L2 cache
│   ├── transaction-internals.md  # Proxy mechanics, propagation, isolation levels
│   ├── postgresql-indexing.md    # B-Tree, GIN, EXPLAIN ANALYZE interpretation
│   └── microservices-patterns.md # Gateway, Circuit Breaker (Resilience4j)
├── code-examples/                # Mini-projects and reference implementations
│   ├── secure-rest-api/          # Spring Boot 3 + JWT + RFC 7807 ProblemDetail
│   ├── jpa-n-plus-one/           # Demonstrating and fixing N+1 with EntityGraphs
│   └── transactional-pitfalls/   # Self-invocation and isolation level demos
└── dsa-practice/                 # Month 3 DSA problems (Trees, BSTs, Tree BFS/DFS)
```

## 🎯 Key Study Topics

1. **Spring Core & Spring Boot Internals:**
   - IoC, Constructor Injection, Bean Lifecycle callbacks, Bean Scopes.
   - Auto-configuration mechanics (`@EnableAutoConfiguration`, `AutoConfiguration.imports`).
   - Spring Boot Actuator, Micrometer metrics, `@ConfigurationProperties`.
2. **REST APIs & Web Layer:**
   - Request dispatching (`DispatcherServlet`), `@RestController`, DTO validation.
   - Global exception handling with `@RestControllerAdvice` and RFC 7807 `ProblemDetail`.
   - OpenAPI 3 / Swagger documentation.
3. **Spring Security & Authentication:**
   - `SecurityFilterChain`, stateless JWT authentication filter, OAuth2/OIDC flows.
   - Role-Based Access Control (RBAC), method security with `@PreAuthorize`.
4. **Spring Data JPA & Hibernate Performance:**
   - Entity states (Transient, Managed, Detached, Removed), relationship mappings.
   - Eliminating the N+1 problem (`JOIN FETCH`, `@EntityGraph`, batch size).
   - Hibernate First-Level (L1) and Second-Level (L2) cache.
5. **Transactions & Database Concurrency:**
   - Spring `@Transactional` proxy mechanics, self-invocation bypass.
   - Propagation rules (`REQUIRED`, `REQUIRES_NEW`), Isolation levels, Read phenomena.
   - Optimistic locking (`@Version`) vs. Pessimistic locking (`PESSIMISTIC_WRITE`).
6. **SQL & PostgreSQL Database Tuning:**
   - B-Tree index mechanics, GIN indexes, composite indexes, `EXPLAIN ANALYZE` execution plans.
   - Advanced SQL: CTEs, Window functions, table partitioning, HikariCP pool tuning.
7. **Microservices Architecture:**
   - Spring Cloud Gateway, Service Discovery, OpenFeign, Resilience4j (Circuit Breaker).
8. **DSA (Target: 25–30 problems, Cumulative: 75–90):**
   - Binary Trees, BSTs, Tree Traversals (BFS, DFS), LCA, Path Sum, Tree Diameter.

## 🏆 Monthly Milestone
- Build a secure, production-ready Spring Boot microservice with JWT authentication and RFC 7807 errors.
- Master `@Transactional` propagation, isolation levels, and solve JPA N+1 query bottlenecks.
- Interpret PostgreSQL `EXPLAIN ANALYZE` output to optimize query performance and index design.
- Reach 75–90 solved DSA problems, with strong command of tree algorithms.
