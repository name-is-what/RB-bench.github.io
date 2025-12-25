# 🧩 Model RB Benchmark Suite

Benchmarks with Hidden Optimum Solutions for  
**SAT, CSP, Graph Problems, Set Covering, Set Packing, and Winner Determination**

---

## 👋 Overview

This repository hosts a curated collection of **benchmark instances based on Model RB**, a random model with exact phase transitions and provable hardness properties.  
The benchmarks are designed with **hidden optimum solutions**, making them particularly suitable for evaluating both **complete and incomplete algorithms** on hard instances.

The benchmark families included here cover a broad range of classical NP-hard problems, including:

- Boolean Satisfiability (SAT)
- Constraint Satisfaction Problems (CSP)
- Maximum Independent Set (MIS)
- Minimum Vertex Cover (MVC)
- Maximum Clique and Vertex Coloring
- Minimum Set Covering (MSC)
- Maximum Set Packing (MSP)
- Winner Determination in Combinatorial Auctions
- Pseudo-Boolean Optimization
- Weighted Max-2-SAT

All benchmark constructions are derived from **Model RB**, whose theoretical properties have been extensively studied in the literature.

---

## 🧪 Benchmark Collections

The benchmark suite is organized into the following categories:

- **Forced Satisfiable CSP and SAT Benchmarks**  
  Hard satisfiable instances generated at the exact phase transition of Model RB.

- **Graph Benchmarks with Hidden Optimum Solutions (BHOSLIB)**  
  Benchmarks for MIS, MVC, Maximum Clique, and Vertex Coloring, obtained via transformations from Model RB SAT instances.

- **Set Covering, Set Packing, and Winner Determination Benchmarks**  
  Instances transformed from graph benchmarks, with hidden optimal solutions preserved.

- **Pseudo-Boolean (0–1 Integer Programming) Benchmarks**  
  Instances with known optimal solutions derived from Model RB constructions.

- **Weighted Max-2-SAT Benchmarks**  
  Weighted SAT instances with hidden optima for evaluating Max-SAT solvers.

Detailed descriptions, theoretical background, and downloadable instances for each category are provided on the documentation website.

---

## 📰 News

Historical experimental results, solver performance records, and benchmark usage statistics are preserved in the documentation, including:

- SAT Competition and CSP Solver Competition usage
- Long-term hardness records on large graph instances
- Updates reported by researchers using these benchmarks

---

## ⬇️ Downloads

All benchmark instances are provided as compressed archives (`.tar.gz`, `.gz`) and are available through the documentation pages.

- SAT / CSP benchmarks in **DIMACS CNF** and CSP formats  
- Graph benchmarks in **ASCII DIMACS** and **binary DIMACS** formats  
- Set covering and packing benchmarks in a DIMACS-style set format  

> Benchmark files are stored under `docs/assets/bench/` and linked directly from the documentation pages.

---

## 📚 Documentation

The full documentation is built with **GitHub Pages** and organized as a multi-page site:

👉 **Documentation site:**  
`https://RandomBinaryCSP.github.io/`

The documentation includes:

- Formal problem definitions
- Benchmark generation models
- File format descriptions
- Download links
- Lists of papers that use each benchmark family

---

## 📖 References

The benchmarks in this repository are based on the following foundational works:

- K. Xu and W. Li. *Exact Phase Transitions in Random Constraint Satisfaction Problems*. JAIR, 2000.
- K. Xu and W. Li. *Many Hard Examples in Exact Phase Transitions*. TCS, 2006.
- K. Xu et al. *Random Constraint Satisfaction: Easy Generation of Hard (Satisfiable) Instances*. AIJ, 2007.

See individual benchmark pages for complete reference lists.

---

## 📬 Contact

If you have comments, questions, or would like to contribute additional benchmark results or references, please feel free to get in touch.

---

*This repository serves as a long-term, stable home for Model RB benchmark instances and related documentation.*
