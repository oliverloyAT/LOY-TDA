LOY-TDA: Topological Market Fragility Framework
This repository implements the Loy Taxonomy, a framework using Topological Data Analysis (TDA) to identify structural instabilities in financial markets.

📊 Validation Renders
The engine identifies "Topological Singularities" (drops in Persistence Entropy) that serve as leading indicators for market stress.

1997 Vintage Validation (Asian Financial Crisis)
2026 Modern Snapshot (S&P 500)
🛠 Setup (macOS ARM64)
1. System Requirements
Bash
brew install openblas pkg-config
2. Environment & Dependencies
Bash
python3.12 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
🚀 Trading Operations
Generate Daily Signal
python3.12 lab_v26.py

Strategy Logic
Stable State: Entropy Z-Score > -1.5 (Risk-On)

Fragile State: Entropy Z-Score < -2.0 (Hedge / Exit)

📜 License & Disclaimer
License: Apache License 2.0

Disclaimer: This is for research and strategy development. Trading involves significant risk. The Loy Taxonomy is a probabilistic model; past topological signatures do not guarantee future results.

📚 Citation
Loy, O. (2026). Topological Signatures of Financial Fragility.
