---
layout: default
title: Weighted Max-2-SAT Benchmarks with Hidden Optimum Solutions
parent: Benchmarks Based on Model RB
nav_order: 5
---

# Weighted Max-2-SAT Benchmarks with Hidden Optimum Solutions

If you have any comments or need more instances for the following Max-2-SAT benchmarks, please send me an email.

---

The Maximum Satisfiability Problem (Max-SAT), an optimization version of SAT, is the problem of finding an assignment that maximizes the number of satisfied clauses. Max-SAT is NP-hard even if every clause contains at most two literals (called the Max-2-SAT problem). Weighted Max-SAT is a generalization of Max-SAT in which every clause has a weight and the goal is to find an optimum assignment maximizing the total weight of satisfied clauses. Finding challenging benchmarks for the (weighted) Max-SAT problem is not only of significance for the experimental evaluation of (weighted) Max-SAT algorithms but also of interest to the theoretical computer science community. The weighted Max-2-SAT benchmarks presented here are transformed from forced satisfiable SAT benchmarks of Model RB. In fact, based on Model RB and this transformation, we can propose a simple model for generating random weighted Max-2-SAT instances as follows (Thanks to Chu-Min Li for discussions):

---

## Generation Model

First generate $n$ disjoint sets of boolean variables, each of which has cardinality $n^\alpha$ (where $\alpha>0$ is a constant), and then for every variable $x$, generate a unit clause $x$, and for every two variables $x$ and $y$ in the same set, generate a 2-clause $\lnot x \vee \lnot y$.

Randomly select two different disjoint sets and then generate without repetitions $pn^{2\alpha}$ clauses of the form $\lnot x \vee \lnot z$ where $x$ and $z$ are two variables selected at random from these two sets respectively (where $0<p<1$ is a constant);

Run Step 2 (with repetitions) for another $rn\ln n-1$ times (where $r>0$ is a constant);

For every unit clause, we have a weight equal to $1$, and for every 2-cluase, we have a weight equal to $i$ (where $i=$ the total number of unit clauses $+1$).

---

## Properties

The goal is to maximize the total weight of satisfied clauses. For the random Max-2-SAT model above, since the weight of every 2-clause is greater than the total weight of unit clauses, it is not hard to see that for any optimum assignment, every 2-clause must be satisfied and in such a case, at most $n$ unit clauses can be satisfied (one from each disjoint set). Therefore, the maximum value of the total weight of satisfied clauses is at most $n+i*m$ where $m$ is the number of 2-clauses. Interestingly, determining if such a upper bound can be reached is equivalent to determining the satisfiability of the corresponding CSP and SAT instances of Model RB, and there is a one-to-one mapping between the solutions of these two problems. To hide an optimum assignment in the instances of the Max-2-SAT model above, we first select a boolean variable at random from each disjoint set to form a set of $n$ variables which take value $1$, and then in the above process of generating random clauses (Step 2), no clause is allowed to violate this hidden optimum assignment. From the results of the paper "Many Hard Examples in Exact Phase Transitions with Application to Generating Hard Satisfiable Instances", it is expected that Model RB can also be used to generate hard instances for Max-SAT algorithms (by use of the above Max-2-SAT model and the hardness of phase transitions, i.e. choosing appropriate values of $\alpha$, $p$ and $r$). Recently, it has been shown (both experimentally and theoretically) that unlike random 3-SAT, it is quite natural and easy to hide solutions in random CSP and SAT instances of Model RB. For more details, please see an IJCAI-05 paper entitled "A Simple Model to Generate Hard Satisfiable Instances".

---

## Format

Note: The following weighted Max-2-SAT benchmarks are expressed in the DIMACS format and the optimum value is given in the first line of each file.

---

## Benchmarks

- [`frb30-15-wcnf.tar.gz`](../assets/bench/frb30-15-wcnf.tar.gz) (248 KB): 450 Boolean variables - 5 instances, with the optimum value = $30 + 451m$ (where $m$ is the number of 2-clauses)
- [`frb35-17-wcnf.tar.gz`](../assets/bench/frb35-17-wcnf.tar.gz) (390 KB): 595 Boolean variables - 5 instances, with the optimum value = $35 + 596m$ (where $m$ is the number of 2-clauses)
- [`frb40-19-wcnf.tar.gz`](../assets/bench/frb40-19-wcnf.tar.gz) (578 KB): 760 Boolean variables - 5 instances, with the optimum value = $40 + 761m$ (where $m$ is the number of 2-clauses)
- [`frb45-21-wcnf.tar.gz`](../assets/bench/frb45-21-wcnf.tar.gz) (822 KB): 945 Boolean variables - 5 instances, with the optimum value = $45 + 946m$ (where $m$ is the number of 2-clauses)
- [`frb50-23-wcnf.tar.gz`](../assets/bench/frb50-23-wcnf.tar.gz) (1148 KB): 1150 Boolean variables - 5 instances, with the optimum value = $50+1151m$ (where $m$ is the number of 2-clauses)
- [`frb53-24-wcnf.tar.gz`](../assets/bench/frb53-24-wcnf.tar.gz) (1352 KB): 1272 Boolean variables - 5 instances, with the optimum value = $53+1273m$ (where $m$ is the number of 2-clauses)
- [`frb56-25-wcnf.tar.gz`](../assets/bench/frb56-25-wcnf.tar.gz) (1574 KB): 1400 Boolean variables - 5 instances, with the optimum value = $56+1401m$ (where $m$ is the number of 2-clauses)
- [`frb59-26-wcnf.tar.gz`](../assets/bench/frb59-26-wcnf.tar.gz) (1824 KB): 1534 Boolean variables - 5 instances, with the optimum value = $59+1535m$ (where $m$ is the number of 2-clauses)

---

Remark: The feedback from several researchers indicates that the above benchmarks might be too hard for current solvers. So, in what follows, we added some benchmark sets of smaller size. (New!)

---

## Smaller Benchmarks

- [`frb10-6-wcnf.tar.gz`](../assets/bench/frb10-6-wcnf.tar.gz) (7 KB): 60 Boolean variables - 5 instances, with the optimum value = $10 + 61m$ (where $m$ is the number of 2-clauses)
- [`frb15-9-wcnf.tar.gz`](../assets/bench/frb15-9-wcnf.tar.gz) (35 KB): 135 Boolean variables - 5 instances, with the optimum value = $15 + 136m$ (where $m$ is the number of 2-clauses)
- [`frb20-11-wcnf.tar.gz`](../assets/bench/frb20-11-wcnf.tar.gz) (78 KB): 220 Boolean variables - 5 instances, with the optimum value = $20 + 221m$ (where $m$ is the number of 2-clauses)
- [`frb25-13-wcnf.tar.gz`](../assets/bench/frb25-13-wcnf.tar.gz) (147 KB): 325 Boolean variables - 5 instances, with the optimum value = $25 + 326m$ (where $m$ is the number of 2-clauses)

---

List of Papers That Use MAX-SAT Benchmarks Based on Model RB (Updated: Mar. 4, 2009)

---

## Other Benchmarks Based on Model RB

- [Forced Satisfiable CSP and SAT Benchmarks of Model RB](forced-sat-csp.md)
- [Benchmarks with Hidden Optimum Solutions for Graph Problems](hidden-opt-graph.md)
- [Pseudo-Boolean (0-1 Integer Programming) Benchmarks with Hidden Optimum Solutions](pseudo-boolean.md)
- [Benchmarks with Hidden Optimum Solutions for Set Covering, Set Packing and Winner Determination](set-covering.md)

---

Back to Ke Xu's homepage.