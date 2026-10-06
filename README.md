# Eliyahu Dahan

**Data Analyst | End-to-End Data Systems | GT-First Methodology**

Independent. Self-taught. Building data systems from scratch.

Before every project, I validate feasibility: API, labels, Ground Truth. 
When GT exists – full validation. When it doesn't – I document it and 
build alternative validation.

---

## Projects

### 🚆 Metrodorf v2 – Train Delay Prediction (Infrabel, Belgium)
**Status:** Completed.

Predicting train delays on line IC 16-1 (Brussels ↔ Luxembourg corridor).

**Pipeline:** 45.6M training records (2023–2024, Infrabel Open Data, CC0) · 1.07M rows for IC 16-1
**GT:** DELAY_ARR — measured by Infrabel in seconds, verified (187s = 3:07)
**Target:** arrival ≥360 seconds late (6 min) — anchored in official KPI P.II1

**Results (Test Set — January 2025, untouched until final evaluation):**

| Model | Precision | Recall | F1 |
|-------|-----------|--------|-----|
| Baseline (persistence t-1) | 0.8894 | 0.8878 | 0.8886 |
| LightGBM | 0.9462 | 0.9051 | 0.9252 |

- Confusion matrix: TP=4,347 · FN=456 · FP=247 · TN=41,524
- Improvement over baseline: **+3.66 pp F1**
- Challenger LSTM: F1=0.9110 — did not justify added complexity
- Overfitting gap: 0.0249 — healthy

**Documented lessons:**
- Empirical validation beats assumption — always
- Leakage can look like success (F1=0.97 → 0.92 after removing leaked feature)
- Feature engineering beats representation learning on tabular data
- The test set is sacred — January 2025 stayed untouched

**Dashboard:** [metrodorf-6qxjae77w35b9xhjpilwxc.streamlit.app](https://metrodorf-6qxjae77w35b9xhjpilwxc.streamlit.app/)
**Repository:** [metrodorf](https://github.com/eliyahudahan/metrodorf)

---

### ⚓ Deviative – Maritime Encounter Detection (AIS)
**Status:** Completed.

Detecting dangerous vessel encounters in San Pedro Bay using physics-based DCPA/TCPA analysis.

- 14M pairs → 4,372 anomalies (1.03%) · 22× noise reduction
- Train 1.45% | Test 0.91% — stable across Out-of-Time split
- GT: Task Mismatch documented (4 datasets reviewed, none match)
- Alternative validation: stability, sensitivity, 10 manual cases

**Dashboard:** [deviative-78pbkz3ortv2d6kqvpzfhw.streamlit.app](https://deviative-78pbkz3ortv2d6kqvpzfhw.streamlit.app/)
**Repository:** [deviative](https://github.com/eliyahudahan/deviative)

---

## Tech

**Python** · Pandas · NumPy · Scikit-learn · LightGBM · XGBoost · 
FastAPI · Docker · Streamlit · PostgreSQL · Git

**Methodology:** GT validation · Target before modeling · Time-series split · 
Leakage detection · Sensitivity · Documented limitations

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/eliyahu-dahan-684b22294)
- [GitHub](https://github.com/eliyahudahan)