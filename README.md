# 🌦️ Weather Forecasting and BBQ Suitability Classification using LSTM, XGBoost, and SVM

This project applies time series **forecasting** and **binary classification** techniques to weather data—focusing specifically on **temperature mean (`tempmean`)** and **precipitation (`precip`)**—using Python and Jupyter Notebooks. The goal is to predict weather trends and classify each day as either **suitable for a BBQ (`True`)** or **not suitable (`False`)** based on forecasted conditions.

---

## 📁 Dataset Description

This dataset was created for machine learning and deep learning training purposes. It is suitable for **regression**, **classification**, and **forecasting** tasks. The dataset is complex enough to illustrate real-world challenges such as **overfitting**, **seasonality**, and **imbalanced classes**, while remaining intuitively accessible.

### 🔗 Source Acknowledgment

The original weather data was obtained from:

> **European Climate Assessment & Dataset (ECA&D)**  
> File created on: 22-04-2021  
> Official site: [http://www.ecad.eu](http://www.ecad.eu)

When using this dataset, please acknowledge the following publication:

> Klein Tank, A.M.G. and Coauthors, 2002.  
> *Daily dataset of 20th-century surface air temperature and precipitation series for the European Climate Assessment.*  
> International Journal of Climatology, 22, 1441–1453.

---

## 🎯 Target Labels

After forecasting temperature and precipitation, the model classifies each day into one of the following binary labels:

- **`True`** — Suitable for BBQ (e.g., warm temperature, low precipitation)
- **`False`** — Not Suitable for BBQ (e.g., rain, cold, or high humidity)

These labels are derived using rule-based thresholds on the predicted values, such as:
- `tempmean` above a comfortable threshold (e.g., 22°C)
- `precip` below a tolerable limit (e.g., 1 mm)

---

## ⚙️ Methods Used

### 🔮 Forecasting Models
- **LSTM** (Long Short-Term Memory Neural Network)
- **XGBoost** (Extreme Gradient Boosting)

### 🧠 Classification Model
- **SVM** (Support Vector Machine)

Forecasting models are used to predict future weather values (`tempmean`, `precip`). The classification model (SVM) then evaluates the forecasted values and assigns a binary BBQ suitability label.

---

## 📈 Results Overview

| Target     | Forecasting Models | Classification Model |
|------------|--------------------|----------------------|
| tempmean   | LSTM, XGBoost      | SVM                  |
| precip     | LSTM, XGBoost      | SVM                  |

Model performance is evaluated using:
- **RMSE** for forecasting accuracy
- **Classification Accuracy**, **Confusion Matrix** for BBQ suitability classification

---

## 📦 Files Included

| File Name                  | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| `lstm_svm_tempmean.ipynb` | Forecast `tempmean` using LSTM, then classify BBQ suitability using SVM     |
| `lstm_svm_precip.ipynb`   | Forecast `precip` using LSTM, then classify BBQ suitability using SVM       |
| `xgb_svm_tempmean.ipynb`  | Forecast `tempmean` using XGBoost, then classify BBQ suitability using SVM  |
| `xgb_svm_precip.ipynb`    | Forecast `precip` using XGBoost, then classify BBQ suitability using SVM    |
| `weather_prediction_dataset.csv`                | Weather dataset used for modeling                                 |
| `weather_prediction_bbq_labels.csv`                | Weather dataset bbq labels                                |
| `README.md`               | Project overview and documentation                                          |

