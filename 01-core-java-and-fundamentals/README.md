# Month 1 — Core Java and Fundamentals

> **Timeline:** October 2026  
> **Target Proficiency:** ⭐⭐⭐⭐⭐  
> **Master Roadmap:** [6-Month-Interview-Roadmap.md](../6-Month-Interview-Roadmap.md#october-2026--core-java-and-fundamentals) | [Repository README](../README.md)

---

## 📌 Module Overview

Month 1 establishes foundational mastery of the Java language, memory mechanics, object-oriented design principles, the Collections framework internals, modern functional programming constructs, and foundational Data Structures & Algorithms (DSA).

## 📂 Recommended Directory Structure

```text
01-core-java-and-fundamentals/
├── notes/                     # In-depth conceptual notes and whiteboard diagrams
│   ├── oop-and-memory.md      # Memory layout, pass-by-value, immutability
│   ├── collections-internals.md # HashMap bucket collision, ConcurrentHashMap
│   ├── generics-and-pecs.md   # Generics wildcards, type erasure, PECS rule
│   ├── exceptions.md          # Exception hierarchy, try-with-resources
│   └── java8-functional.md    # Stream pipelines, collectors, Optional patterns
├── code-examples/             # Hands-on code demonstrations
│   ├── collections/           # Custom HashMap / LRU Cache implementation
│   ├── streams/               # Complex groupingBy / partitioningBy examples
│   └── immutability/          # Defensive copy and immutable class patterns
└── dsa-practice/              # Month 1 algorithmic problems (Arrays, Two Pointers, Sliding Window)
```

## 🎯 Key Study Topics

1. **Core Java & Memory Model:**
   - Stack vs. Heap allocation, pass-by-value semantics.
   - `Object` class contracts: `equals()`, `hashCode()`, `toString()`, `clone()`.
   - String interning, String Pool mechanics, `String` vs. `StringBuilder` vs. `StringBuffer`.
2. **Collections Framework Internals:**
   - `List` (`ArrayList` resizing formula, `LinkedList`).
   - `Map` (`HashMap` hashing, treeification to Red-Black tree at threshold 8, `ConcurrentHashMap` CAS + sync).
   - `Set` (`HashSet`, `TreeSet`, `LinkedHashSet`).
   - `Comparable` vs. `Comparator`, Fail-Fast vs. Fail-Safe iterators.
3. **Generics & Type Erasure:**
   - Bounded types, PECS (`Producer Extends Consumer Super`).
   - Bridge methods, type erasure, and generic arrays.
4. **Exception Handling:**
   - Hierarchy (`Throwable` -> `Error` / `Exception` -> `RuntimeException`).
   - `try-with-resources`, `AutoCloseable`, and suppressed exceptions.
5. **Java 8+ Functional Programming:**
   - Functional interfaces (`Predicate`, `Function`, `Consumer`, `Supplier`).
   - Stream API pipelines, advanced `Collectors.groupingBy()`.
   - `Optional` anti-patterns and safe usage idioms.
6. **DSA (Target: 25–30 problems):**
   - Arrays, Strings, Two Pointers, Sliding Window, Prefix Sum, Hash Maps.

## 🏆 Monthly Milestone
- Fluently explain Java memory allocation and the `equals()`/`hashCode()` contract in live interviews.
- Code a custom `HashMap` and LRU Cache from scratch.
- Master complex Stream collectors and solve 25–30 high-frequency array/string problems.
