# ML-Cardiac Anomaly Classifier | AED Intelligence

## 📌 Project Overview
This project focuses on developing a high-precision classification model for **Automated External Defibrillators (AED)**. These devices must analyze electrocardiogram (ECG) rhythms in real-time to decide if a life-saving electric shock is required.

The goal was to build a robust model capable of distinguishing between **Normal Rhythms (0)** and **Abnormal/Affected Rhythms (1)** based on 30 complex ECG parameters.

## 📊 Dataset & Features
The analysis utilized a dataset containing 30 parameters derived from ECG signals:
- **Temporal Metrics:** TCI, TCSC, MAV, etc.
- **Spectral Features:** VF filter (vFleak), Spectral moments (M, A1-A3).
- **Complexity Metrics:** Sample Entropy (SamEn), Hilbert Transform (HILB), and Kurtosis.

## 🛠️ Data Science Pipeline
1. **Exploratory Data Analysis (EDA):** Identified feature distributions and high correlation (collinearity) between spectral variables.
2. **Pre-processing:** Applied "Capping" for outlier management and StandardScaler for feature normalization.
3. **Model Selection:**
   - **Logistic Regression:** Selected as the production-ready model due to its interpretability and perfect performance on validation.
   - **Random Forest:** Used as a benchmark for non-linear relationship detection.
4. **Validation:** Tested against a blind dataset (`data_onu.csv`).

## 📈 Key Results
- **Recall (Sensitivity): 1.00** — Crucial for medical devices, ensuring no cardiac anomalies are missed (Zero False Negatives).
- **Accuracy & Precision:** Exceeded the 85% requirement, reaching near-perfect classification on the provided validation set.

## 📂 Repository Structure
- `/notebooks`: `M7_Marcel_Palma_Parte I_DEA.ipynb` (Full analysis and modeling).
- `/data`: Training (`data_reto.csv`) and Validation (`data_onu.csv`) datasets.
- `/docs`: Project requirements and case description.

## 🚀 Technologies Used
- **Python** (Pandas, NumPy)
- **Scikit-Learn** (LogisticRegression, RandomForestClassifier, Metrics)
- **Matplotlib & Seaborn** (Data Visualization)
