---
layout: page
permalink: /research/
title: research
description: Research in algorithms and data structures.
nav: true
nav_order: 1
---

My research asks two related questions: how efficiently can classical algorithmic problems be solved, and what guarantees remain when an algorithm does not have complete information? Across my projects, I look for the structure that determines the answer. Implementations and small examples often reveal that structure; the goal is then to turn it into an algorithm or a rigorous limitation.

## Sublinear matching algorithms

**With Professor Seth Pettie, University of Michigan**

We studied whether matching algorithms that inspect only a small part of a graph behave as their theoretical guarantees might suggest. Our team built a reproducible framework for evaluating six randomized and deterministic algorithms on bipartite regular, random regular, and Erdős–Rényi graphs with as many as $10^8$ vertices. I implemented the Dani–Hayes, Gabow, Hopcroft–Karp, and Goel–Kapralov–Khanna algorithms.

My main contribution was an adversarial family of regular graphs for the Dani–Hayes algorithm. The construction repeatedly draws its random walk into regions that do not reveal a useful augmenting path. On tested instances of degree at least 16, the algorithm made more than 9.7 billion random-neighbor probes without finding the next augmentation within 300 seconds. We then used the construction to show that this style of random walk cannot produce a matching of size $\frac{n}{2}(1-o(\frac{1}{d+1}))$ on certain $d$-regular graphs within $O(dn)$ time. This work led to the manuscript _Giving Sublinear Matching Algorithms a Reality Check_.

## Online memory allocation

**Senior thesis with Professor Nicole Wein, University of Michigan**

When requests arrive and depart online and stored data cannot be moved, an allocator may need to split a request across several free regions. We study the inverse tradeoff: if memory use must remain within a factor of $1+\varepsilon$ of optimal, how much fragmentation is unavoidable? Let $M$ be the maximum live volume and $Q$ the maximum number of simultaneous requests. We proved that an allocator can require $\Omega((1+\varepsilon^{-1})Q)$ fragments.

For the lower bound, we constructed an adaptive workload that repeatedly removes selected requests and replaces them with a larger one. A potential records the number of contiguous occupied runs; the probabilistic method shows that every round has a replacement choice that increases this potential. We also designed a paging algorithm using $O((1+\varepsilon^{-1})Q)$ fragments. By choosing a page size near $\varepsilon M/Q$, it leaves at most one partially filled page per live request and keeps wasted capacity within the permitted overhead. The upper and lower bounds match asymptotically. I also investigated what guarantees remain possible when the workload parameters are not known in advance.

## Deterministic satisfiability algorithms

**With Professor Cliff Liu, Shanghai Jiao Tong University**

We worked on simplifying and improving deterministic algorithms for $k$-SAT. I replaced a 38-case comparison in the analysis of a 2018 algorithm with a recursive framework based on overlapping clauses. By expressing the cost of a clause chain through a recurrence on shorter chains, I showed that the single-clause chain is the most expensive case. This makes the analysis easier to verify and allows richer overlap structures to be evaluated without rebuilding the original case split.

We then used bounded-size blocks of overlapping clauses to constrain the assignment space more strongly. The resulting deterministic 3-SAT algorithm runs in $1.32736^n$ time, improving the previous $1.32793^n$ bound. I also helped extend the framework to $k\geq 4$; our analysis gives bases of $1.49824$ for 4-SAT and $1.59935$ for 5-SAT. The full argument appears in the preprint [_Improved Deterministic Algorithms for k-SAT: Generalization of Chains and Recurrence Proof_](https://arxiv.org/abs/2611.16814).
