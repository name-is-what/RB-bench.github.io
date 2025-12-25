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
`https://RB-bench.github.io/`

The documentation includes:

- Formal problem definitions
- Benchmark generation models
- File format descriptions
- Download links
- Lists of papers that use each benchmark family

---

## 📖 References  
### Selected Papers about Model RB

- **Ke Xu and Wei Li.**  
  [Exact Phase Transitions in Random Constraint Satisfaction Problems.](assets/pdf/JAIR00.pdf)  
  *Journal of Artificial Intelligence Research*, 12 (2000): 93–103.

- **Ke Xu and Wei Li.**  
  [Many Hard Examples in Exact Phase Transitions.](assets/pdf/TCS06.pdf)  
  *Theoretical Computer Science*, 355 (2006): 291–302.  
  Earlier version: CoRR Report cs.CC/0302001, Feb. 2003.

- **Ke Xu, Frederic Boussemart, Fred Hemery and Christophe Lecoutre.**  
  [Random Constraint Satisfaction: Easy Generation of Hard (Satisfiable) Instances.](assets/pdf/AIJ07.pdf)  
  *Artificial Intelligence*, 171 (2007): 514–534.  
  Earlier version appeared in Proc. of the 19th IJCAI, pp. 337–342, Scotland, 2005.

- **Ke Xu and Guangyan Zhou.**  
  [SAT Requires Exhaustive Search.](assets/pdf/SAT_requires_exhaustive_search.pdf)  
  *Frontiers of Computer Science*, Volume 19, Article 1912405, 2025.

- **Ke Xu and Guangyan Zhou.**  
  [Self-reference as key to proving extreme hardness — Reply to the comment by Allender and Williams.](assets/pdf/Self-reference_as_key_to_proving_extreme_hardness.pdf)

---

## 📬 Contact

For questions, comments, or requests for additional benchmark instances, please contact: **kexu AT buaa.edu.cn**

---

*This repository serves as a long-term, stable home for Model RB benchmark instances and related documentation.*
