
# 🔧 Predictive Maintenance System Using Machine Learning

A data-driven machine learning project that predicts machine failures using high-frequency sensor data, historical maintenance logs, and machine metadata. This system supports proactive maintenance scheduling, minimizes unplanned downtime, and helps optimize operational efficiency.

---

## 📌 Project Highlights

- ✅ **Failure Prediction** using Random Forest with 0.90+ AUC-ROC
- ✅ **Sensor Fusion** from temperature, vibration, pressure, and runtime
- ✅ **Rolling Feature Engineering** with 7-day & 14-day averages
- ✅ **Risk Assessment Dashboard** with Low/Medium/High categorization
- ✅ **Automated Maintenance Scheduling** based on risk and overhaul history
- ✅ **Cost Savings Simulation** from failure prevention

---

## 🧠 Problem Statement

Industrial machines often fail without warning, causing expensive downtime and emergency repairs. By analyzing patterns in machine sensor data and historical repairs, this project aims to predict failures in advance and recommend timely maintenance actions.

---

## 📁 Dataset Overview

The system uses three CSV datasets:

| Dataset | Description |
|---------|-------------|
| `Sensor_Readings.csv` | Real-time data on Temperature, Vibration, Pressure, Runtime |
| `Maintenance_Logs.csv` | History of machine failures, repairs, downtime |
| `Machine_Metadata.csv` | Info about machine type, age, and overhaul dates |

---

## 📊 Key Features & Workflow

### 1. **Data Cleaning & Preprocessing**
- Imputation for missing values (`Vibration`, `RepairType`)
- Standardization of date formats
- Outlier handling using IQR method

### 2. **Feature Engineering**
- Daily aggregation of sensor data
- Rolling averages (7-day, 14-day) for trend analysis
- Calculated time since last overhaul
- One-hot encoding of machine types

### 3. **Target Variable Creation**
- Binary classification: failure within next 30 days (1 or 0)

### 4. **Model Training**
- Random Forest Classifier (`class_weight='balanced'`)
- Stratified train-test split
- Scaled features using `StandardScaler`

### 5. **Model Evaluation**
- **AUC-ROC:** 0.907 ✅
- **Recall:** 0.96 (high sensitivity to failure detection)
- **Confusion Matrix & ROC Curve Visualizations**

### 6. **Maintenance Recommendation Engine**
- Classifies machines into **Low / Medium / High Risk**
- Schedules maintenance based on:
  - Failure probability
  - Risk level
  - Days since last overhaul

---

## 📈 Results

| Metric          | Score     |
|-----------------|-----------|
| AUC-ROC         | 0.907     |
| Precision       | 0.23      |
| Recall          | 0.96      |
| Estimated Failures Prevented | 6100+ |
| Cost Savings Estimate        | $61M+ |

---

## 🛠️ Tech Stack

- **Language**: Python 3
- **Libraries**: pandas, NumPy, scikit-learn, seaborn, matplotlib, BeautifulSoup
- **Model**: Random Forest Classifier
- **IDE**: Jupyter Notebook

---

## 📂 Folder Structure

```bash
predictive_maintenance/
│
├── data/
│   ├── Sensor_Readings.csv
│   ├── Maintenance_Logs.csv
│   └── Machine_Metadata.csv
│
├── outputs/
│   ├── maintenance_schedule.csv
│   ├── feature_importance.csv
│   └── risk_assessment.csv
│
├── visuals/
│   ├── roc_curve.png
│   ├── feature_importance.png
│   └── maintenance_timeline.png
│
├── predictive_maintenance_analysis.ipynb
└── README.md
```

---

## 📌 Business Impact

By proactively identifying high-risk machines, this system helps:
- Avoid unexpected breakdowns
- Reduce operational downtime
- Prioritize maintenance based on data
- Save millions in repair and downtime costs

---

## 📅 Next Steps

- ⏱ Integrate with **real-time monitoring systems**
- 📲 Deploy as a **dashboard using Streamlit or Flask**
- 🔔 Implement **email/SMS alerts** for high-risk machines
- 🧠 Experiment with **LSTM / time series models** for further accuracy

---

## 📸 Sample Screenshot

![Dashboard View](./visuals/maintenance_dashboard.png)

---

## 🤝 Let's Collaborate

If you're interested in building a real-time dashboard, automating alerts, or enhancing this system with deep learning, feel free to reach out or fork the project!

---

## 📬 Contact

**Muhammad Abrar**  
📧 abrarofficial@outlook.com  
🌐 [LinkedIn](https://linkedin.com) | [GitHub](https://github.com) | [Portfolio](https://streamlit.site.link)
