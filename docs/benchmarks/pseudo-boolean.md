---
layout: default
title: Pseudo-Boolean (0-1 Integer Programming) Benchmarks with Hidden Optimum Solutions
parent: Benchmarks Based on Model RB
nav_order: 3
---

# Pseudo-Boolean (0-1 Integer Programming) Benchmarks with Hidden Optimum Solutions

If you have any comments or need more instances for the following benchmarks, please send me an email.

---

The Pseudo-Boolean (0-1 integer programming) problem is a linear integer programming problem where all variables are restricted to take values of either 0 or 1. This problem is NP-hard, and as such, it is considered unlikely that there exists an efficient algorithm for solving it. The Pseudo-Boolean (0-1 Integer Programming) benchmarks presented here are transformed from forced satisfiable SAT benchmarks of Model RB, with the set of variables and the set of constraints respectively corresponding to the set of variables and the set of binary clauses in SAT instances. In fact, based on Model RB and this transformation, we can propose a simple random Pseudo-Boolean model as follows:

---

## Generation Model

First generate $n$ disjoint sets of variables, each of which has cardinality $n^\alpha$ (where $\alpha>0$ is a constant), and then for every two variables $x$ and $y$ in the same set, generate a constraint $x + y \leq 1$;

Randomly select two different disjoint sets and then generate without repetitions $pn^{2\alpha}$ constraints of the form $x + z \leq 1$ where $x$ and $z$ are two variables selected at random from these two sets respectively (where $0<p<1$ is a constant);

Run Step 2 (with repetitions) for another $rn\ln n-1$ times (where $r>0$ is a constant).

---

## Properties

The objective function is to maximize the sum of all variables. It is easy to see that for the Pseudo-Boolean model above, the value of the objective function is at most $n$. Interestingly, determining if such a upper bound can be reached is equivalent to determining the satisfiability of the corresponding CSP and SAT instances of Model RB, and there is a one-to-one mapping between the solutions of these two problems. To hide an optimum solution of value $n$ in the instances of this Pseudo-Boolean model, we first select a variable at random from each disjoint set to form a set of $n$ variables which take value $1$, and then in the above process of generating random constraints (Step 2), no constraint is allowed to violate this hidden optimum solution. From the results of the paper "Many Hard Examples in Exact Phase Transitions with Application to Generating Hard Satisfiable Instances", it is expected that Model RB can also be used to generate hard instances for Pseudo-Boolean algorithms (by use of the above Pseudo-Boolean model and the hardness of phase transitions, i.e. choosing appropriate values of $\alpha$, $p$ and $r$). Recently, it has been shown (both experimentally and theoretically) that unlike random 3-SAT, it is quite natural and easy to hide solutions in random CSP and SAT instances of Model RB. For more details, please see an IJCAI-05 paper entitled "A Simple Model to Generate Hard Satisfiable Instances".

---

## Format

Note: The following Pseudo-Boolean (0-1 Integer Programming) benchmarks are expressed in the opb format which can be found on PBLIB.

---

## Benchmarks

- [`frb30-15-opb.tar.gz`](../assets/bench/frb30-15-opb.tar.gz) (447 KB): 450 variables (30 disjoint sets) - 5 instances, with the optimum value = 30
- [`frb35-17-opb.tar.gz`](../assets/bench/frb35-17-opb.tar.gz) (693 KB): 595 variables (35 disjoint sets) - 5 instances, with the optimum value = 35
- [`frb40-19-opb.tar.gz`](../assets/bench/frb40-19-opb.tar.gz) (1029 KB): 760 variables (40 disjoint sets) - 5 instances, with the optimum value = 40
- [`frb45-21-opb.tar.gz`](../assets/bench/frb45-21-opb.tar.gz) (1459 KB): 945 variables (45 disjoint sets) - 5 instances, with the optimum value = 45
- [`frb50-23-opb.tar.gz`](../assets/bench/frb50-23-opb.tar.gz) (2021 KB): 1150 variables (50 disjoint sets) - 5 instances, with the optimum value = 50
- [`frb53-24-opb.tar.gz`](../assets/bench/frb53-24-opb.tar.gz) (2381 KB): 1272 variables (53 disjoint sets) - 5 instances, with the optimum value = 53
- [`frb56-25-opb.tar.gz`](../assets/bench/frb56-25-opb.tar.gz) (2774 KB): 1400 variables (56 disjoint sets) - 5 instances, with the optimum value = 56
- [`frb59-26-opb.tar.gz`](../assets/bench/frb59-26-opb.tar.gz) (3211 KB): 1534 variables (59 disjoint sets) - 5 instances, with the optimum value = 59

---

## News

In 2005, according to weblog statistics, this webpage was visited 4330 times (by people from 46 countries) and the above benchmarks were downloaded 445 times. Most visitors were from USA, China, Canada, UK, India, France, Germany, Australia, Italy and Spain (about 1/3 of them came through Google).

The above benchmarks were used for Pseudo Boolean Evaluation 2005 (8 solvers) and Pseudo Boolean Evaluation 2006 (14 solvers). The results are summarized in following table where the "Best Value (2005)" and "Best Value (2006)" respectively represent the best values obtained in the competition by the competing solvers in 2005 (the timeout is 20 minutes) and in 2006 (the timeout is 30 minutes).

---

## Results

| Instance          | frb30-15-1 | frb30-15-2 | frb30-15-3 | frb30-15-4 | frb30-15-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 30         | 30         | 30         | 30         | 30         |
| Best Value (2005) | 30         | 30         | 30         | 30         | 30         |
| Best Value (2006) | 30         | 30         | 30         | 30         | 30         |

| Instance          | frb35-17-1 | frb35-17-2 | frb35-17-3 | frb35-17-4 | frb35-17-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 35         | 35         | 35         | 35         | 35         |
| Best Value (2005) | 34         | 33         | 34         | 35         | 33         |
| Best Value (2006) | 35         | 35         | 35         | 35         | 35         |

| Instance          | frb40-19-1 | frb40-19-2 | frb40-19-3 | frb40-19-4 | frb40-19-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 40         | 40         | 40         | 40         | 40         |
| Best Value (2005) | 38         | 38         | 38         | 37         | 38         |
| Best Value (2006) | 40         | 39         | 40         | 40         | 39         |

| Instance          | frb45-21-1 | frb45-21-2 | frb45-21-3 | frb45-21-4 | frb45-21-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 45         | 45         | 45         | 45         | 45         |
| Best Value (2005) | 41         | 41         | 41         | 42         | 41         |
| Best Value (2006) | 44         | 44         | 44         | 45         | 44         |

| Instance          | frb50-23-1 | frb50-23-2 | frb50-23-3 | frb50-23-4 | frb50-23-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 50         | 50         | 50         | 50         | 50         |
| Best Value (2005) | 46         | 45         | 45         | 46         | 46         |
| Best Value (2006) | 49         | 49         | 49         | 49         | 49         |

| Instance          | frb53-24-1 | frb53-24-2 | frb53-24-3 | frb53-24-4 | frb53-24-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 53         | 53         | 53         | 53         | 53         |
| Best Value (2005) | 49         | 48         | 49         | 48         | 48         |
| Best Value (2006) | 52         | 52         | 51         | 51         | 51         |

| Instance          | frb56-25-1 | frb56-25-2 | frb56-25-3 | frb56-25-4 | frb56-25-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 56         | 56         | 56         | 56         | 56         |
| Best Value (2005) | 49         | 49         | 50         | 50         | 49         |
| Best Value (2006) | 54         | 54         | 54         | 54         | 54         |

| Instance          | frb59-26-1 | frb59-26-2 | frb59-26-3 | frb59-26-4 | frb59-26-5 |
| ----------------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| Optimum Value     | 59         | 59         | 59         | 59         | 59         |
| Best Value (2005) | 52         | 52         | 51         | 52         | 53         |
| Best Value (2006) | 57         | 57         | 57         | 57         | 57         |

---

[List of Papers That Use PB Benchmarks Based on Model RB](other/list-pb-papers.md) (Updated: Mar. 4, 2009)

---

## Other Benchmarks Based on Model RB

- [Forced Satisfiable CSP and SAT Benchmarks of Model RB](forced-sat-csp.md)
- [Benchmarks with Hidden Optimum Solutions for Graph Problems](hidden-opt-graph.md)
- [Benchmarks with Hidden Optimum Solutions for Set Covering, Set Packing and Winner Determination](set-covering.md)
- [Weighted Max-2-SAT Benchmarks with Hidden Optimum Solutions](weighted-max2sat.md)