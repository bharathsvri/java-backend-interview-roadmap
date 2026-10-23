# Month 2 — Concurrency and JVM

> **Timeline:** Month 2 (Self-Paced / 4 Weeks)  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#month-2--concurrency-and-jvm) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 2 focuses on high-concurrency systems programming, the Java Memory Model (JMM), thread synchronization constructs, asynchronous pipelines with `CompletableFuture`, JVM runtime architecture, garbage collection algorithms, and modern features through Java 21+ Virtual Threads.

## 📂 Recommended Directory Structure

```text
02-concurrency-and-jvm/
├── notes/                        # Conceptual deep dives and interview notes
│   ├── java-memory-model.md      # JMM, happens-before, volatile, memory barriers
│   ├── thread-pools.md           # ThreadPoolExecutor tuning, saturation policies
│   ├── completable-future.md     # Async composition and error handling
│   ├── jvm-internals.md          # Runtime data areas, class loaders, JIT
│   ├── gc-algorithms.md          # G1, ZGC, heap tuning, pause-time analysis
│   └── virtual-threads.md        # Loom, carrier threads, pinning caveats
├── code-examples/                # Executable concurrency demonstrations
│   ├── producer-consumer/        # BlockingQueue vs. wait/notify vs. Lock/Condition
│   ├── async-pipelines/          # CompletableFuture composition recipes
│   ├── deadlocks/                # Deadlock simulation, thread dumps, and prevention
│   └── virtual-threads-demo/     # Virtual thread throughput benchmark
└── dsa-practice/                 # Month 2 DSA problems (Linked Lists, Stacks, Binary Search)
```

## 🎯 Key Study Topics

1. **Multithreading & JMM:**
   - Thread states, `synchronized` monitors, `volatile` visibility and memory barriers.
   - Happens-before rules, race conditions, deadlocks, `ThreadLocal` leak prevention.
2. **Modern Concurrency & `CompletableFuture`:**
   - `ThreadPoolExecutor` parameters, bounded queues, and rejection policies.
   - `CompletableFuture` async chaining (`thenApply`, `thenCompose`, `thenCombine`, `allOf`).
   - Synchronization utilities (`CountDownLatch`, `CyclicBarrier`, `Semaphore`, `ReentrantLock`).
   - Atomic variables, CAS mechanics, and `LongAdder`.
3. **JVM Runtime Data Areas:**
   - Heap (Eden, Survivor spaces S0/S1, Old Generation), Metaspace, Stacks, PC Registers, Native Stacks.
   - ClassLoader hierarchy and Parent Delegation model. JIT compiler (C1, C2, Tiered).
4. **Garbage Collection & Tuning:**
   - Generational hypothesis, STW pauses, G1 GC, ZGC, Shenandoah.
   - Diagnostic tools: `jcmd`, `jmap`, JVisualVM, JMC/JFR, `async-profiler`.
   - Analyzing heap dumps, memory leaks, and CPU spikes.
5. **Modern Java (Java 9 to 21+):**
   - Virtual Threads (Project Loom) architecture and pinning issues.
   - Structured Concurrency, Scoped Values, Records, Sealed Classes, Pattern Matching.
6. **DSA (Target: 25–30 problems, Cumulative: 50–60):**
   - Linked Lists (in-place reversal, cycle detection), Monotonic Stacks, Binary Search variations.

## 🏆 Monthly Milestone
- Write production-grade asynchronous pipelines using `CompletableFuture` and tune thread pool sizing.
- Diagnose JVM memory leaks and thread deadlocks using heap dumps and profiling tools.
- Articulate Virtual Threads mechanics vs. platform threads and reach 50–60 solved DSA problems.
