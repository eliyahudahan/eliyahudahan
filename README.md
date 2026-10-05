# Eliyahu Dahan

**Data Analyst | End-to-End Data Systems | GT-First Methodology**

Independent. Self-taught. Building data systems from scratch.

Before every project, I validate feasibility: API, labels, Ground Truth.
When GT exists – full validation. When it doesn't – I document it and 
build alternative validation.

---

## Projects

### ⚓ Deviative – Maritime Encounter Detection (AIS)
**Status:** Completed.

Detecting dangerous vessel encounters in San Pedro Bay using 
physics-based DCPA/TCPA analysis.

- 14M pairs → 4,372 anomalies (1.03%) · 22× noise reduction
- Train 1.45% | Test 0.91% — stable across Out-of-Time split
- GT: Task Mismatch documented (4 datasets reviewed, none match)
- Alternative validation: stability, sensitivity, 10 manual cases
- Dashboard: [deviative-demo.streamlit.app](https://deviative-78pbkz3ortv2d6kqvpzfhw.streamlit.app/)

**Repository:** [deviative](https://github.com/eliyahudahan/deviative)

---

### 🚆 Metrodorf – Train Delay Prediction (Infrabel, Belgium)
**Status:** In progress (pipeline complete, model in development).

- Pipeline: 45.6M records (24 months, Infrabel Open Data)
- GT: DELAY_ARR (measured, verified — 187s = 3:07)
- Target: 360s, anchored in official KPI P.II1 (6 min, 111 measuring points)
- Model in development: LightGBM + persistence baseline (t-168)
- Test set: January 2025, untouched until final evaluation

**Repository:** [metrodorf](https://github.com/eliyahudahan/metrodorf)

---

## Tech

Python · Pandas · NumPy · Scikit-learn · LightGBM · XGBoost · 
FastAPI · Docker · Streamlit · PostgreSQL · Git

**Methodology:** GT validation · Target before modeling · 
Time-series split · Sensitivity · Documented limitations

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/eliyahu-dahan-684b22294)
- [GitHub](https://github.com/eliyahudahan)