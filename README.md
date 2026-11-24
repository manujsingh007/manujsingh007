## Hi, I'm Manuj 👋

**M.Eng. student in AI Engineering of Autonomous Systems at Technische Hochschule Ingolstadt (THI)**
B.Sc. International Business Information Systems, Hochschule Furtwangen

I'm a software developer moving into machine learning engineering. I'm interested in what it takes to put ML into production: reliable data pipelines, honest evaluation, and models that are deployed, monitored and explainable. My focus is industrial and automotive AI: sensor data, condition monitoring and perception.

🔎 **Open to Werkstudent (working student) roles** in ML / AI / data / software engineering, Ingolstadt · Munich · remote
🗣️ English (C2) · German (B2)

---

### 🏭 Featured project

**[Industrial Predictive Maintenance & Failure Intelligence](https://github.com/manujsingh007/industrial-predictive-maintenance)**
Estimates the remaining useful life (RUL) of turbofan engines from multivariate sensor data (NASA C-MAPSS), with calibrated prediction intervals.

- **Result:** test RMSE **14.6 cycles** (95% CI 12.5–16.6) on FD001, about 7 cycles better than a linear baseline; evaluated **once** on the sealed test set under a pre-registered protocol
- **Uncertainty:** 90% prediction intervals via Mondrian conformal prediction (93% empirical test coverage), about ±6 cycles near failure
- **Engineering:** leakage-free engine-level cross-validation, causal window features, LightGBM vs. 1D-CNN comparison, MLflow experiment tracking, architecture decision records, CI with GitHub Actions
- **Error analysis:** the model is accurate near failure (~4 cycles RMSE) but predicts fast-degrading engines too late in mid-life; weaknesses documented with future fixes
- **Serving:** FastAPI service loading the `champion` model from the MLflow registry, PostgreSQL storage (Alembic migrations) for readings and predictions, and a replay simulator that streams test engines cycle by cycle; integration tests run against Postgres in CI
- **Monitoring:** Streamlit fleet dashboard alerting on the interval's lower bound (caught all 16 test engines within 20 cycles of failure, no far-from-failure false alarms) and PSI drift monitoring validated by fault injection
- **Deployment:** the full stack (PostgreSQL, migrations, model training, API, dashboard) starts with one `docker compose up`; CI builds the images; documented with an architecture diagram, model card and four architecture decision records

`Python` `LightGBM` `PyTorch` `scikit-learn` `pandas` `MLflow` `FastAPI` `PostgreSQL` `SQLAlchemy` `Docker Compose` `Streamlit` `pytest` `GitHub Actions`

### 🗺️ Planned

- **Industrial visual inspection:** defect detection and unsupervised anomaly detection on images, with Grad-CAM explanations
- **Evidence-based document RAG:** German/English question answering over technical documents, with citation checking and retrieval evaluation
- **MLOps platform:** automated training, model registry, drift detection and retraining, serving more than one model

---

### 🛠️ Tech I work with

**ML / AI:** Python · PyTorch · scikit-learn · LightGBM · pandas · NumPy
**Backend & engineering:** FastAPI · Java / Spring Boot · REST APIs · SQL / PostgreSQL · TypeScript / React
**MLOps & tooling:** Docker · Git · GitHub Actions (CI/CD) · MLflow · Linux · pytest

---

### 📫 Contact

- **LinkedIn:** [manuj-singh-sansanwal](https://www.linkedin.com/in/manuj-singh-sansanwal-14769a242)
- **Email:** [manujsansanwal2002@gmail.com](mailto:manujsansanwal2002@gmail.com)
