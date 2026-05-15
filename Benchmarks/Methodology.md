# Comparative Performance Report: Set X (100 - 1,000 Nodes)

This folder contains the comparative analysis between the GSL Engine and standard industry baselines: **Clarke-Wright (CW)** and **LNS (Iteration-bounded)**.

## ⚙️ Benchmarking Methodology & Environment
To ensure a fair and transparent comparison, the following constraints were applied:

* **Hardware:** Native execution on a mobile processor (Snapdragon via Pydroid 3).
* **LNS Constraint:** The Large Neighborhood Search (LNS) was strictly bounded to **300 iterations** per instance. This limit simulates a high-pressure, **Real-time** logistics scenario where an immediate response is required.
* **CW Baseline:** Standard Clarke-Wright savings heuristic (constructive).
* **GSL Engine:** Operates under its standard deterministic logic with no iteration-based random search. All instances are 100% verified feasible.

## 📊 Benchmark Results (Sample)
The following table summarizes the performance across different instances based on the % Gap to BKS. Note that GSL prioritizes speed and absolute determinism over extended heuristic searches.

| Instance | BKS | GSL Gap | CW Gap | LNS Gap (300 Iter) | GSL vs LNS Winner |
| :--- | :--- | :--- | :--- | :--- | :--- |
| X-n125-k30 | 55539.0 | **+4.28%** | +5.92% | +6.30% | **GSL** |
| X-n176-k26 | 47812.0 | **+4.42%** | +9.91% | +13.35% | **GSL** |
| X-n247-k50 | 37274.0 | **+9.31%** | +9.53% | +13.50% | **GSL** |
| X-n670-k130 | 146332.0 | **+7.38%** | +8.46% | +25.32% | **GSL** |

## 📈 Technical Findings
* **Win Rate vs LNS:** GSL maintains a strong **71% win rate** compared to LNS (300 iter) across Set X, demonstrating superior performance when time and computing power are constrained.
* **Win Rate vs CW:** While CW achieves a lower overall cost gap in the majority of basic instances, GSL outperforms CW in specific high-complexity topologies.
* **Consistency:** GSL provides high-precision results in **Real-time**, whereas metaheuristics (LNS) show higher variance under restricted iterations.
* **Deterministic Execution:** The structured logic ensures predictable output quality regardless of the environment.

