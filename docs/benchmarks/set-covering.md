---
layout: default
title: Benchmarks with Hidden Optimum Solutions for Set Covering, Set Packing and Winner Determination
parent: Benchmarks Based on Model RB
nav_order: 4
---

# Benchmarks with Hidden Optimum Solutions for Set Covering, Set Packing and Winner Determination

If you have any comments or need more instances for the following benchmarks, please send me an email.

---

## Minimum Set Covering (MSC) and Maximum Set Packing (MSP)

Given a universe $U$ and a collection $C$ of subsets of $U$, a set cover is a subset $S$ of $C$ such that the union of $S$ is $U$ (i.e. each element in $U$ belongs to at least one member of $S$), while a set packing is a collection of mutually disjoint subsets $S$ of $C$. The minimum set covering problem (also minimum set cover problem) is to find a set cover with the smallest number of subsets, while the maximum set packing problem is to find a set packing with the largest number of subsets. These two problems are NP-hard, and as such, it is considered unlikely that there exists efficient algorithms for solving them.

Finding challenging benchmarks for the minimum set covering problem and the maximum set packing problem is not only of significance for experimentally evaluating the algorithms of solving these two problems but also of interest to the theoretical computer science community. The MSC and MSP benchmarks presented here are directly transformed from maximum independent set benchmarks with hidden optimum solutions (which are transformed from forced satisfiable SAT benchmarks of Model RB).

More specifically, given a graph $G$, we can transform $G$ into a collection $C$ of subsets by mapping each vertex into a subset which consists of the edges connecting to the vertex. It is easy to see that if a graph has $n$ vertices and the size of its maximum independent sets is $m$ (or equivalently speaking, the size of its minimum vertex covers is $n-m$), then for the collection of subsets transformed, the size of minimum set covers and the size of maximum set packings are respectively equal to the size of minimum vertex covers and the size of maximum independent sets of the original graph. In such a way, we obtain MSC and MSP benchmarks with hidden optimum solutions.

In fact, based on Model RB and this transformation, we can propose a simple model for generating random MSC and MSP instances as follows.

First generate $n^{\alpha+1}$ empty subsets uniformly divided into $n$ groups (where $\alpha>0$ is a constant), i.e. each group has $n^{\alpha}$ empty subsets. A subset pair is an unordered pair of two subsets. Every different subset pair is indexed by a different number. Then, for every subset pair whose two subsets are in the same group, put its index number in its two subsets.

Randomly select two different groups and then uniformly select without repetitions $p n^{2\alpha}$ subset pairs (where $0<p<1$ is a constant) from $n^{2\alpha}$ possible ones (each of which consists of two subsets respectively from these two groups). For every selected pair, put its index number in its two subsets.

Run Step 2 (with repetitions) for another $r n \ln n - 1$ times (where $r>0$ is a constant).

It is easy to see that for the random model above, the size of maximum set packings is at most $n$ (because every two subsets in the same group have at least one common element). Interestingly, determining if such an upper bound can be reached is equivalent to determining the satisfiability of the corresponding CSP and SAT instances of Model RB, and there is a one-to-one mapping between the solutions of these two problems. To hide an optimum solution of value $n$ in the instances of the above model, we first select a subset at random from each group to form a hidden solution of size $n$, and then in the above process of selecting random pairs of subsets (Step 2), no pair is allowed to violate this hidden solution.

From the results of the paper *Many Hard Examples in Exact Phase Transitions with Application to Generating Hard Satisfiable Instances*, it is expected that Model RB can also be used to generate hard instances for set covering and set packing algorithms (by use of the above model and the hardness of phase transitions, i.e. choosing appropriate values of $\alpha$, $p$ and $r$). It is also hoped that the method of hiding solutions based on Model RB can have potential applications in cryptography. Recently, it has been shown (both experimentally and theoretically) that unlike random 3-SAT, it is quite natural and easy to hide solutions in random CSP and SAT instances of Model RB. For more details, please see an IJCAI-05 paper entitled *A Simple Model to Generate Hard Satisfiable Instances*.

---

## File Format

As far as we know, there is no standard format to express the minimum set covering and maximum set packing problems. Based on the ASCII DIMACS graph format, we propose a format for these two problems as follows.

There are 0 or more lines starting with `c` at the top of the file which are comment lines and can be ignored.

Following the comment lines, there is a line with the form `p set U S`, where $U$ and $S$ are respectively the number of elements in the universe (denoted by natural numbers) and the number of subsets in the collection.

The remaining of the file is a list of lines starting with `s` which indicate the subsets in the collection (e.g. the line `s 1 2 4` indicates that there is a subset with three elements which are 1, 2 and 4).

**Note:** All the benchmarks provided here are expressed in the above format.

---

## Downloads (MSC / MSP)

- [`frb30-15-msc.tar.gz`](../assets/bench/frb30-15-msc.tar.gz) (419 KB): 450 subsets — 5 instances, with the size of the MSC = 420 and the size of the MSP = 30
- [`frb35-17-msc.tar.gz`](../assets/bench/frb35-17-msc.tar.gz) (666 KB): 595 subsets — 5 instances, with the size of the MSC = 560 and the size of the MSP = 35
- [`frb40-19-msc.tar.gz`](../assets/bench/frb40-19-msc.tar.gz) (990 KB): 760 subsets — 5 instances, with the size of the MSC = 720 and the size of the MSP = 40
- [`frb45-21-msc.tar.gz`](../assets/bench/frb45-21-msc.tar.gz) (1412 KB): 945 subsets — 5 instances, with the size of the MSC = 900 and the size of the MSP = 45
- [`frb50-23-msc.tar.gz`](../assets/bench/frb50-23-msc.tar.gz) (1943 KB): 1150 subsets — 5 instances, with the size of the MSC = 1100 and the size of the MSP = 50
- [`frb53-24-msc.tar.gz`](../assets/bench/frb53-24-msc.tar.gz) (2281 KB): 1272 subsets — 5 instances, with the size of the MSC = 1219 and the size of the MSP = 53
- [`frb56-25-msc.tar.gz`](../assets/bench/frb56-25-msc.tar.gz) (2677 KB): 1400 subsets — 5 instances, with the size of the MSC = 1344 and the size of the MSP = 56
- [`frb59-26-msc.tar.gz`](../assets/bench/frb59-26-msc.tar.gz) (3110 KB): 1534 subsets — 5 instances, with the size of the MSC = 1475 and the size of the MSP = 59

---

## Winner Determination in Combinatorial Auctions

In a combinatorial auction, there is a set of indivisible bids with prices, each of which is a bundle of items. The Winner Determination Problem (WDP) is to choose a collection of bids with maximum surplus such that every item will be assigned to at most one bid. Given a maximum set packing problem, if each subset is viewed as a bid in the winner determination problem and the price of each bid is set to 1, then the maximum surplus is equal to the size of maximum set packings. Thus, the above benchmarks can also be used as benchmarks with hidden optimum solutions for the winner determination problem.

---

## Other Benchmarks Based on Model RB

- [Forced Satisfiable CSP and SAT Benchmarks of Model RB](forced-sat-csp.md)
- [Benchmarks with Hidden Optimum Solutions for Graph Problems](hidden-opt-graph.md)
- [Pseudo-Boolean (0-1 Integer Programming) Benchmarks with Hidden Optimum Solutions](pseudo-boolean.md)
- [Weighted Max-2-SAT Benchmarks with Hidden Optimum Solutions](weighted-max2sat.md)
