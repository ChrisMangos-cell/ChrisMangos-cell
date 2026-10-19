# Hi, I'm Chris 👋

Data Analyst & Analytics Engineer focused on building resilient data pipelines, econometric measurement systems, and applied machine learning models.

---

### 🛠️ Core Technical Stack

- **Languages & Querying:** Python (Pandas, NumPy, SciPy, Requests), SQL (DuckDB, BigQuery)
- **Data Engineering & Architecture:** DuckDB OLAP Star-Schema Marts, Columnar Parquet Storage, Prefect DAGs, GitHub Actions (CI/CD), Idempotent Upserts, Stateful Watermarking
- **Analytics & Econometric Modeling:** Bayesian Non-Linear Marketing Mix Modeling (MMM), Geometric Adstock Decay, Hill Saturation Dynamics, Non-Linear Constrained Optimization (SLSQP, L-BFGS-B), Statistical Anomaly Detection
- **Machine Learning & Algorithms:** Scikit-Learn (HistGradientBoosting, Classifiers, PCA, k-Means), SHAP (TreeExplainer), Vector Search (Cosine Similarity), Non-Parametric Outlier Detection (MAD, Tukey's Fences)
- **BI, Product Serving & APIs:** FastAPI, Uvicorn, Pydantic v2, Streamlit, Plotly, Tableau, Looker Studio

---

### 🚀 Featured Engineering & Analytics Projects

- **[Meridian-Lite: Enterprise Marketing Mix Modeling & Budget Optimization Platform](https://github.com/ChrisMangos-cell/marketing_incrementality_mmm)**  
  End-to-end econometric measurement and capital allocation engine designed to bypass post-iOS 14.5 ad-attribution signal loss.
  - **Data Engineering:** Engineered a 728-day continuous DuckDB analytical star schema (`dim_calendar`, `dim_channels`, `fact_spend`, `fact_revenue`) compiled into compressed Parquet marts.
  - **Applied Econometrics:** Implemented vectorized Geometric Adstock memory carryover and Hill saturation curves with analytical first-order derivatives ($\text{mROAS}$).
  - **Model Performance:** Solved a 33-parameter regularized MAP optimization via L-BFGS-B achieving **$R^2 = 90.53\%$**, **$\text{MAPE} = 3.57\%$**, and **$\text{RMSE} = \$1,914.87$**.
  - **Capital Optimization:** Deployed a non-linear SLSQP solver that identified **$173,077/year** in misallocated ad spend (siphoning capital from saturated Google P-Max into under-attributed channels), unlocking **+4.96% incremental revenue** with **$0 added ad spend**.
  - **Production Delivery:** Built an interactive multi-tab Streamlit decision cockpit and validated pipeline integrity with 20 deterministic Pytest unit/integration tests.

- **[Healthcare Clinical Risk Prediction API](https://github.com/ChrisMangos-cell/data-portfolio/tree/main/healthcare_risk_api)**  
  Production-grade machine learning microservice predicting cardiovascular disease risk across a cohort of 69,823 biologically validated clinical profiles.
  - **Data Engineering & Cleaning:** Implemented a DuckDB SQL staging pipeline enforcing biological sanity bounds (filtering 177 physiological anomalies where `systolic_bp < diastolic_bp` or vitals fell out-of-range) across 70,000 raw patient records into clean Parquet storage.
  - **Predictive Performance:** Trained an optimized `HistGradientBoostingClassifier` achieving **0.8633 ROC-AUC** and **0.8645 PR-AUC** on stratified holdouts.
  - **Clinical Decision Tuning:** Lowered the classification decision threshold from 0.50 to 0.40 to prioritize clinical sensitivity, **reducing missed critical cases by 32.9%** (false negatives dropped from 1,586 to 1,064) with an F1-score of 0.7877.
  - **Explainable AI (XAI):** Integrated SHAP `TreeExplainer` to extract individual risk attributions, isolating systolic blood pressure and age as the dominant drivers increasing risk (+2 to +4 log-odds) and physical activity as a primary protective factor.
  - **Microservice Serving & Test Guardrails:** Built containerized FastAPI/Uvicorn endpoints (`/predict`, `/predict/batch`) with Pydantic v2 validation enforcing dynamic BMI computation and cross-field vitals checks, fully backed by an automated Pytest test suite asserting HTTP 422 rejection of incoherent data.

- **[E-Commerce Revenue & Retention Engine](https://github.com/ChrisMangos-cell/data-portfolio)**  
  Multi-year cohort retention analysis (`< 0.7%` repeat purchase decay), RFM customer segmentation identifying **~R$ 4.4M** in dormant GMV, and an interactive Streamlit BI application for executive scenario planning.

- **[Global Weather Pipeline & Anomaly Engine](https://github.com/ChrisMangos-cell/data-portfolio)**  
  Resilient API ingestion layer with exponential backoff, stateful watermarking, idempotent DuckDB storage, Prefect DAG orchestration, and automated daily CI/CD cron jobs.

- **[Spotify Music Clustering & Vector Recommender](https://github.com/ChrisMangos-cell/data-portfolio)**  
  Unsupervised ML pipeline clustering 32,800+ tracks into 6 acoustic archetypes using PCA variance retention (84.08%) and sub-second Cosine Similarity vector search.
