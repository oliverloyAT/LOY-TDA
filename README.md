cat << 'EOF' > README.md
# LOY-TDA: Topological Market Fragility & Trading Framework

This repository implements the **Loy Taxonomy**, a high-performance framework utilizing **Topological Data Analysis (TDA)** to detect systemic market fragility. By monitoring the evolution of simplicial complexes in residualized asset returns, this engine identifies "Topological Singularities" that serve as leading indicators for market crashes.

## 📊 Performance Validation
The engine identifies "Topological Singularities" (drops in Persistence Entropy) that serve as leading indicators for market stress.

### Real-Time Analysis Snapshot (2024–2026)
![2026 Dashboard](paper_topology_dashboard.jpg)

### Historical Crisis Validation (1997)
![1997 Dashboard](vintage_1997_dashboard.jpg)

---

## 🛠 Setup (macOS ARM64)

### 1. System Requirements
The TDA backends (`giotto-tda`, `ripser`) require C++ compilation tools and optimized BLAS libraries.

```bash
brew install openblas pkg-config
```
### 2. Environment & Dependencies
This framework requires Python 3.12.

```bash
# Create and activate virtual environment
python3.12 -m venv venv
source venv/bin/activate

# Install locked dependencies
pip install -r requirements.txt
```


### Trading Operations
# 1. Generate Core Market Signature
```bash
python3.12 market_topology.py
```
# 2. Live Diagnostic and Singularity Check
To run the full 2026 diagnostic lab, pull live data, and check for active Topological Singularities:
```bash
python3.12 lab_v26.py
```

## 📊 Historical Benchmarks (Tested & Utilized in Paper)

The following events were used to validate the Loy Taxonomy. These specific dates represent the "Real-Time Snapshots" where the engine identifies transitions between Type I (Structural) and Type II (Velocity) regimes.

| Event Description | Snapshot Date (`as_of`) |
| :--- | :--- |
| 1997: Type II: Contagion Singularity | 1997-10-27 |
| 2002: Type 1 Dot Crash | 2002-10-08 |
| 2008: Type 1 (Pre-Lehman) | 2008-09-11 |
| 2008: Systematic Collapse (Trough) | 2009-03-06 |
| 2010: Event Horizon | 2010-05-05 |
| 2010: Flash Event | 2010-05-06 |
| Pre-Volmageddon 2018: Type 2 | 2018-02-02 |
| Volmageddon: Type 2 | 2018-02-05 |
| 2020: Type 1 (Pandemic Disturbance) | 2020-03-20 |
| **Present: 2026 Baseline** | **2026-04-28** |

Changing Analysis Dates:
To backtest specific dates or update the live diagnostic, modify the following lines (and a bit more) in the source code:
* **Lab Diagnostic:** Edit line `34` in `lab_v26.py`
* **Core Engine:** Edit line `566` in `market_topology.py`
Strategy Logic
The trading signal is derived from the Persistence Entropy Z-Score (Panel IV/V):

🟢 Stable State (Risk-On): Entropy Z-Score > -1.5

🔴 Fragile State (Hedge / Exit): Entropy Z-Score < -2.0

### License & Disclaimer
License: Apache License 2.0

Disclaimer: This software is for research and strategy development purposes only. Trading financial instruments involves significant risk. The "Loy Taxonomy" is a probabilistic model; past topological signatures do not guarantee future market outcomes.

### Citation
If using this framework or the S4 Velocity metrics, please cite:
Loy, O. (2026). "Topological Signatures of Financial Fragility."
EOF
