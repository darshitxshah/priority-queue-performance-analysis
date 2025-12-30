# Empirical Performance Analysis of Priority Queues

## Overview
This project compares two foundational data structures for implementing
priority queues: binary heaps and unbalanced binary search trees (BSTs).

While both structures offer logarithmic-time operations in theory, their
practical performance differs significantly depending on input patterns
and workload composition. This project evaluates those differences through
controlled benchmarking experiments.

---

## Implementations
- **Binary Heap:** Implemented using Python’s `heapq`
- **Binary Search Tree:** Custom unbalanced BST

Each structure supports insert, find-min, and delete-min operations and is
tested under identical conditions.

---

## Folder Structure

```
priority_queue_project/
├── report/
│   └── ds2239_priority_queues_report.pdf    # Final report (PDF version)
│
├── src/
│   └── main.ipynb                           # Full code notebook with implementations, benchmarks, and plots
│
└── README.md                                # You're reading this!
```

---

## How to Run the Code

1. Make sure Python 3 is installed.
2. Install required libraries:

```bash
pip install matplotlib pandas
```

3. Launch the notebook:

```bash
jupyter notebook src/main.ipynb
```

---

## Benchmarking Setup

The notebook benchmarks the two data structures under the following mixed operation workloads:

- 70% insert / 30% delete
- 50% insert / 50% delete
- 30% insert / 70% delete

Each test consists of **1000 operations**, with performance measured using `time.perf_counter()`.

---

## Results Summary
- Binary heaps consistently outperformed BSTs across all workloads.
- BST insert performance degraded significantly in insert-heavy scenarios due
  to structural imbalance.
- Delete-min operations in BSTs were less sensitive to imbalance, but still
  slower than heap-based implementations.
- Results empirically confirm theoretical worst-case behavior of unbalanced BSTs.

---

## Research Integration

This project is informed by the 2025 study:

**Ma, Lejun & Yuan, Yue & Wang, Huan & Liu, Huihui & Wu, Qiuling. (2025). Evaluation of Priority Queues in the Priority Flood Algorithm for Hydrological Modelling. Water. 17. 10.3390/w17223202**  
[Read it on ResearchGate](https://www.researchgate.net/publication/397442669)

The paper shows that while heaps perform well in general, structures like **pairing heaps** and **HHeap** offer better efficiency in domain-specific large-scale tasks.

---

## Academic Context

This project was completed as part of a graduate-level course in Data Structures and Algorithms and has been refactored for professional and portfolio use.

---

## 💡 Potential Extensions

- Implement AVL Tree or Red-Black Tree as a self-balancing alternative to BST
- Add pairing heap or hash-heap (HHeap) for advanced comparisons
- Simulate larger workloads (10,000+ operations)
- Explore cache-aware optimizations or GPU-based PQs

---

## License

MIT License

---

## Author
**Darshit Shah**  
Master’s in Data Science  
