# Credit-Portfolio-IRB-Analysis
IFR9 Parameters estimation with Random Forest Model. This code was inspired by a Kaagle notebook. Here is the link of the source:  https://www.kaggle.com/code/kwigan/01-credit-portfolio-advancedirb-v1.

The dataset combines anonymized real-world client information with synthetic parameters to preserve confidentiality while maintaining realistic portfolio dynamics.

## Credit Portfolio Stress Testing with Basel III Advanced IRB and AI/ML
### Context
Machine Learning for portfolio PDs wasn’t prohibited in banking — it was just impractical under SR 11-7, TRIM, and IRB requirements (explainability, validation, documentation, stress-testability). Only in recent years, with regulatory clarification and better engineering stacks, ML has become feasible.

### Regulatory Shift
* **EBA**: 2021 Discussion Paper + 2023 follow-up
* **PRA**: SS1/23
* **US Regulators**: Interagency RFI
* **ECB**: 2025 Guide (includes ML section)

### Key Challenges
* Aligning PIT/TTC PDs with Basel IRB formulas
* Integrating ML PDs into IFRS 9 staging without instability
* Stress-testing PDs across macro, climate, liquidity shocks
* Ensuring explainability & challenger validation

### Solution Highlights
* **Vectorized IRB Engine** → Basel III RWA & capital ratios for 10K obligors <10s
* **PIT/TTC PD Scenarios** → base / stress / severe
* **IFRS 9 ECL Staging** → Stage 1 vs Stage 2+ provisions
* **Climate Overlay** → orderly / disorderly / hot-house pathways
* **Monte Carlo Losses** → 10K correlated default sims, VaR/ES @99%
* **ML PD Models** → RandomForest + governance with Fast TreeSHAP (\~3x faster)
* **Liquidity Metrics** → LCR & NSFR with simulated outflows
* **Concentration Risk** → HHI by sector, country, rating
* **Basel Compliance Dashboard** → Capital, Tier 1, Leverage
* **Economic Capital** → sector-level capital allocation
