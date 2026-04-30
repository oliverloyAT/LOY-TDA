cat << 'EOF' > README.md
# LOY-TDA: Topological Market Fragility & Trading Framework

This repository implements the **Loy Taxonomy**, a high-performance framework utilizing **Topological Data Analysis (TDA)** to detect systemic market fragility. By monitoring the evolution of simplicial complexes in residualized asset returns, this engine identifies "Topological Singularities" that serve as leading indicators for market crashes.

## 📊 Performance Validation
The engine identifies "Topological Singularities" (drops in Persistence Entropy) that serve as leading indicators for market stress.

### Real-Time Analysis Snapshot (2024–2026)
![2026 Dashboard](paper_topology_dashboard.jpg)

## 🛠 Setup (macOS ARM64)

### 1. System Requirements
The TDA backends (`giotto-tda`, `ripser`) require C++ compilation tools and optimized BLAS libraries.
\`\`\`bash
brew install openblas pkg-config
\`\`\`

### 2. Environment & Dependencies
This framework requires **Python 3.12**.
\`\`\`bash
# Create and activate virtual environment
python3.12 -m venv venv
source venv/bin/activate

# Install locked dependencies
pip install -r requirements.txt
\`\`\`

---

## 🚀 Trading Operations

### Generate Daily Signal
To generate the current market signature and check for Singularities:
\`\`\`bash
python3.12 lab_v26.py
\`\`\`

### Strategy Logic
The trading signal is derived from the **Persistence Entropy Z-Score** (as seen in Panel IV of the dashboard):

* **Stable State (Risk-On):** Entropy Z-Score $> -1.5$
* **Fragile State (Hedge / Exit):** Entropy Z-Score $< -2.0$

---

## 📜 License & Disclaimer
**License:** Apache License 2.0

**Disclaimer:** This software is for research and strategy development purposes only. Trading financial instruments involves significant risk. The "Loy Taxonomy" is a probabilistic model; past topological signatures do not guarantee future market outcomes.

## 📚 Citation
If using this framework or the S4 Velocity metrics, please cite:
**Loy, O. (2026). "Topological Signatures of Financial Fragility."**
EOF
