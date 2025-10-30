# 🛫 Airline Passenger Forecast (Time Series Forecasting using LSTM)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 📘 Overview

This project demonstrates **time series forecasting** on the classic [AirPassengers](https://datamarket.com/data/set/22u3/airline-passenger-numbers-1949-1960) dataset.  
Using **time series decomposition** and a **Long Short-Term Memory (LSTM)** model, it forecasts the number of airline passengers for the next 12 months.

The project provides insights into **trend**, **seasonality**, and **long-term growth patterns** of air travel demand.

---

## 🧩 Features

- 🗓️ Load and preprocess monthly airline passenger data  
- 🔍 Decompose time series into trend, seasonal, and residual components  
- 🧠 Build and train an **LSTM-based** forecasting model  
- 📈 Predict and visualize **next 12 months** of airline passengers  
- 🎨 Generate informative visualizations for analysis  

---

## 🛠️ Tech Stack

**Language:** Python  
**Libraries Used:**
- `pandas`, `numpy` – Data handling  
- `matplotlib`, `seaborn` – Visualization  
- `statsmodels` – Time series decomposition  
- `scikit-learn` – Data scaling  
- `tensorflow.keras` – LSTM neural network  

---

## ⚙️ Workflow

### **1. Data Loading & Preprocessing**
- Load the `AirPassengers.csv` dataset  
- Convert the `Month` column to datetime format  
- Normalize passenger data using `MinMaxScaler`  

---

### **2. Time Series Decomposition**
Using `seasonal_decompose`:  
- Breaks the series into **Trend**, **Seasonality**, and **Residuals**  
- Helps visualize hidden patterns in the data  

---

### **3. Sequence Generation**
Creates rolling windows of **12 months (`time_step=12`)** for LSTM training.

---

### **4. Model Architecture**
A two-layer **LSTM model** is built using Keras.  

**Training Configuration:**
- **Optimizer:** Adam  
- **Loss Function:** Mean Squared Error (MSE)  
- **Epochs:** 100  
- **Batch Size:** 16  

---

### **5. Forecasting**
Once trained, the model predicts the **next 12 months** of passenger traffic.  
Predicted values are **inverse-transformed** to return to the original scale.

---

### **6. Visualization**
Two main visualizations are created:
- **Decomposition Results** — observed data, trend, seasonality, and residuals  
- **Forecast Plot** — combined historical (blue) and predicted (red) passenger counts  

---

✅ *This workflow covers the entire pipeline — from raw data to visual forecast — demonstrating both statistical and deep learning-based time series modeling.*

---

