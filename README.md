# GeoGuardian: AI-Driven Tourist Safety System 🛡️

**Smart India Hackathon (SIH) 2025 Prototype**

GeoGuardian is a hybrid machine learning system designed to enhance tourist safety by combining real-time location tracking with static user profiling. The system assigns dynamic safety scores and detects movement anomalies to prevent mishaps in real-time.

> **Current Scope:** Calibrated and tested on geospatial data for **Ernakulam District, Kerala**.

## 📂 Repository Structure
This repository contains two core analysis notebooks:
1.  `Dynamic_Model_LSTM.ipynb` - Handles real-time path anomaly detection.
2.  `Static_Model_RF_NN.ipynb` - Handles user profiling and risk assessment.

---

## 🧠 System Architecture

### 1. Dynamic Safety Model (LSTM)
* **Input:** Continuous streams of Latitude & Longitude data (Time-series).
* **Model:** Long Short-Term Memory (LSTM) Network.
* **Function:**
    * Learns "normal" travel patterns and routes within the Ernakulam region.
    * Detects **Path Anomalies**: Deviations from safe/standard routes.
    * Detects **Movement Anomalies**: Sudden stops or erratic speed changes indicative of danger.

### 2. Static Profiling Engine (Random Forest & Neural Networks)
* **Input:** User demographics (Age, Group Type: *Single, Family, Youngsters*) and Location Metadata.
* **Model:** Hybrid Random Forest Classifier + Neural Network.
* **Function:**
    * **User Profiling:** Categorizes the vulnerability of the tourist group.
    * **Location Scoring:** Assigns safety scores to specific coordinates based on historical data and environmental factors.
    * **Risk Calculation:** Combines the User Profile + Location Score to generate a baseline "Risk Index."

---

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Deep Learning:** TensorFlow / Keras (LSTM, Dense Layers)
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Data Processing:** Pandas, NumPy
* **Geospatial:** Geopy (for distance/coordinate calculation)

---

## 🚀 How to Run
Since these are Jupyter Notebooks, the easiest way to run them is via **Google Colab**:

1.  **Clone the repo:**
    ```bash
    git clone [https://github.com/your-username/GeoGuardian.git](https://github.com/your-username/GeoGuardian.git)
    ```
2.  **Open in Colab:**
    * Upload `anomaly_lstm.ipynb` or `Static_Model_RF_NN.ipynb` to [Google Colab](https://colab.research.google.com/drive/1s6i2VbNJ6n6oESLVi_yvprIYdgc6kwU3?authuser=1#scrollTo=ixoa4iB6-uyq) [Google Colab](https://colab.research.google.com/drive/1p6OvG0fEQ9tny6VkvY_lNTmPTd0_5-xQ#scrollTo=7p2sJtFyl7Zr).
3.  **Upload Data:**
    * Ensure you upload the accompanying dataset (CSV files) to the Colab session storage before running the cells.
    * *Note: The model is currently trained on Ernakulam geospatial datasets.*

---

## 🔮 Future Roadmap
* Scale geospatial training data to cover all of Kerala.
* Integrate with a Flutter/React Native frontend for a user-facing mobile app.
* Implement real-time SOS triggering based on LSTM anomaly confidence scores.

---
*Developed by R SANJAY for SIH 2025.*
