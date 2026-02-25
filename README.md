# Hi, I'm Julian Brödnow

Applied Data Science student at **Nordakademie Hamburg**, with a focus on machine learning engineering, temporal modelling, and production-ready data pipelines.

---

## About Me

- Currently finishing my applied data science degree at Nordakademie Hamburg
- My work sits at the intersection of **data engineering**, **ML engineering**, and **analytics**
- I care about building models that are honest — proper temporal validation, no data leakage, reproducible results
- Based in **Hamburg, Germany**

---

## Featured Projects

### [Mapping Shrinking Villages in Rural Japan](https://github.com/jxlianbr/thesis-shrinkin-villages) — Master Thesis
> Classifying population decline patterns in Tohoku, Japan, using satellite imagery, remote sensing, and machine learning

- Integrated **Sentinel-2**, **VIIRS nighttime lights**, **Copernicus DEM**, and **Japanese Census microdata** across 65 sub-municipal units (2015–2025)
- Built a four-stage reproducible pipeline: data acquisition via **Google Earth Engine**, EDA, preprocessing, and classification/typology
- Applied 10 supervised classifiers; best result: **SVM (linear), balanced accuracy 0.662** under strict leakage-controlled conditions
- Unsupervised clustering with bootstrap stability testing (1,000 resamples) and perturbation robustness checks
- Target variable derived from elderly population ratios; top predictors: nighttime light variance, youth demographics, household composition
- YAML-based configuration, type-hinted Python codebase, fully documented data provenance

**Stack:** Python · scikit-learn · XGBoost · geopandas · Google Earth Engine · Sentinel-2 · pandas

---

### Customer Churn Prediction
> Predicting customer churn for a German telecom provider using a temporal sliding-window approach

- Built end-to-end ML pipeline in Python with scikit-learn, deployed on **Microsoft Fabric / Azure Synapse**
- Implemented a **temporal sliding-window** methodology to prevent data leakage across monthly snapshots
- Engineered 30+ features from raw CRM data (tenure, ARPU, contract lifecycle, product flags)
- Trained and compared **Random Forest**, **HistGradientBoosting**, and **Logistic Regression** models; selected best by AUC-ROC
- Primary churn model achieved **94% recall** on a heavily imbalanced dataset (1.4% positive rate)
- Dual-target design: primary churn vs. rotational churn (product switches)
- Integrated **MLflow** experiment tracking and automated model export for production deployment

**Stack:** Python · scikit-learn · pandas · MLflow · Azure AD · Microsoft Fabric · SQL Server

---

### [Urban Traffic Congestion Prediction — Tokyo](https://github.com/jxlianbr/urban-traffic-congestion)
> Short-term vehicle speed forecasting from real-time sensor data in the Tokyo metropolitan area

- Predicts traffic speed at **5, 15, and 30-minute horizons** using live sensor feeds
- Causal feature engineering with explicit lag/rolling statistics to prevent target leakage
- Global time-based train/validation/test splits (no per-segment leakage)
- Primary model: **LightGBM** — Test MAE of 1.55 km/h, R² = 0.918 on 5-min horizon
- Optional **FastAPI** inference server with scheduled retraining pipelines
- ~92 passing **pytest** tests covering data quality and temporal correctness

| Horizon | MAE | RMSE | R² |
|---------|-----|------|-----|
| 5 min | 1.55 km/h | 2.74 km/h | 0.918 |
| 15 min | 1.60 km/h | 2.86 km/h | 0.911 |
| 30 min | 1.72 km/h | 3.09 km/h | 0.896 |

**Stack:** Python · LightGBM · scikit-learn · FastAPI · MLflow · JARTIC WFS API · Open-Meteo

---

## Technical Skills

| Area | Tools & Technologies |
|------|----------------------|
| Machine Learning | scikit-learn · LightGBM · XGBoost · imbalanced-learn |
| Geospatial & Remote Sensing | Google Earth Engine · geopandas · Sentinel-2 · VIIRS · Copernicus DEM |
| Data Engineering | pandas · numpy · SQL Server · Azure Synapse · Microsoft Fabric |
| MLOps | MLflow · joblib · Azure AD · python-dotenv |
| APIs & Services | FastAPI · REST APIs · pyodbc · pymssql |
| Visualisation | matplotlib · seaborn |
| Testing | pytest |
| Languages | Python · SQL |

---

## What I Focus On

- **Temporal correctness** — preventing data leakage in time-series and event-based ML problems
- **Production readiness** — MLflow tracking, reproducible pipelines, clean deployment paths
- **Class imbalance** — handling real-world skewed distributions honestly rather than masking them
- **Interpretability** — feature importance, classification reports, and visual diagnostics as standard outputs

---

## Contact

- LinkedIn: [Julian Brödnow](https://www.linkedin.com/in/julian-br%C3%B6dnow)
- GitHub: [@jxlianbr](https://github.com/jxlianbr)
- Location: Hamburg, Germany
