---
layout: page
permalink: /research/
title: research
description: Current research projects in algorithms and data structures.
nav: true
nav_order: 1
---

## Sublinear matching algorithms

**With Professor Seth Pettie, University of Michigan**

I study whether matching algorithms that inspect only a small part of a graph behave as their analyses predict. Our team built a reproducible framework for evaluating six randomized and deterministic algorithms on bipartite regular, random regular, and Erdős–Rényi graphs with as many as 100 million vertices. I implemented four algorithms and designed an adversarial graph family that exposes a limitation of a random-walk approach. This work led to the manuscript _Giving Sublinear Matching Algorithms a Reality Check_.

## Online memory allocation

**Senior thesis with Professor Nicole Wein, University of Michigan**

When free memory is scattered, an incoming request may have to be divided into several pieces. I study the inverse tradeoff between memory overhead and the number of live fragments required by a nonmoving online allocator. The project combines upper-bound algorithms with adversarial lower-bound constructions and asks what can still be guaranteed when key workload parameters are not known in advance.

## Deterministic satisfiability algorithms

**With Professor Cliff Liu, Shanghai Jiao Tong University**

I work on simplifying and improving deterministic algorithms for k-SAT. Our approach uses recursive descriptions of overlapping clause structures to replace a long case analysis and to refine how the algorithm searches the solution space. My contributions include developing the recursive analysis and helping verify the resulting running-time bounds. This work resulted in the preprint [_Improved Deterministic Algorithms for k-SAT: Generalization of Chains and Recurrence Proof_](https://arxiv.org/abs/2611.16814).

## Broader direction

Across these projects, I am interested in how limited access, memory, and structural information change what an algorithm can achieve. I use experiments to locate failure mechanisms and promising conjectures, then seek proofs that explain whether those observations extend beyond the tested instances.
