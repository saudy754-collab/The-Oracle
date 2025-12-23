# The Oracle of DSCOVR

**The Oracle of DSCOVR** is an AI-powered space weather forecasting project developed during the **NASA Space Apps Challenge 2023**. The project focuses on predicting **solar storms and geomagnetic disturbances** using real-time data from NASA’s **DSCOVR (Deep Space Climate Observatory)** satellite.

Solar storms are not just astronomical phenomena — they directly impact daily life on Earth. Severe events can disrupt:

* ⚡ Electric power grids
* 🛰️ Satellite operations
* 📡 Radio and communication systems
* 🌐 Internet infrastructure

Our goal is to provide an **early warning system** that detects anomalies in solar wind data and predicts geomagnetic storms before they reach Earth.

---

## 🚀 Project Overview

The Oracle uses **machine learning models** to analyze DSCOVR solar wind data and identify abnormal patterns that signal upcoming geomagnetic storms. The system combines:

* **Anomaly Detection** to flag unusual solar behavior
* **Prediction Models** to estimate geomagnetic storm intensity

This hybrid approach improves reliability and reduces false alarms compared to traditional threshold-based systems.

---

## 🛰️ Data Source

We rely on publicly available data from **NASA DSCOVR**, which monitors solar wind parameters from the L1 Lagrange point, including:

* Plasma speed
* Density
* Magnetic field components

These measurements are critical for predicting **Coronal Mass Ejections (CMEs)** and their effects on Earth.

---

## 🧠 System Architecture

![System Architecture](visualizations/system_architecture.png)

> *Figure 1: Overall architecture of The Oracle of DSCOVR showing data ingestion, anomaly detection, and geomagnetic storm prediction pipeline.*

### 1️⃣ Anomaly Detection Model

![Anomaly Detection Workflow](visualizations/anomaly_detection_workflow.png)

> *Figure 2: Anomaly detection process applied to DSCOVR solar wind data.*

The first AI model scans incoming DSCOVR data to detect abnormal behavior in solar wind parameters.

**Key details:**

* **Anomaly threshold:** `0.05`
* **Anomalous samples detected:** `6,984`
* **Normal (good) samples:** `79,117`

Detected anomalies are highlighted and separated from normal data points, forming the basis for further prediction.

---

### 2️⃣ Geomagnetic Storm Prediction Model

Once anomalies are detected, a second AI model predicts the severity of the upcoming geomagnetic storm.

**Performance:**

* **Test RMSE:** `15.46`

This model estimates geomagnetic indices that indicate how strongly Earth’s magnetosphere will be affected.

---

## 📊 Results & Visualization

![Anomaly Detection Results](visualizations/anomaly_results.png)

> *Figure 3: Visualization of detected anomalies (red points) overlaid on normal solar wind data.*

![Prediction Model Performance](visualizations/model2_performance.png)

> *Figure 4: Performance of the geomagnetic storm prediction model (RMSE evaluation).*

* Anomalous data points are overlaid in **red** for clarity
* Normal data points are preserved for trend comparison
* The system cleanly separates noisy signals from meaningful solar events

These visualizations help both scientists and decision-makers quickly understand potential risks.

---

## 🌍 NASA Space Apps Challenge

This project was developed as part of the **NASA Space Apps Challenge 2023**, an international hackathon focused on solving real-world problems using NASA’s open data.

🔗 Project page:
[https://www.spaceappschallenge.org/2023/find-a-team/the-oracle/?tab=project](https://www.spaceappschallenge.org/2023/find-a-team/the-oracle/?tab=project)

---

## 📁 Repository Structure

```
The-Oracle/
│── Anomaly/
    │── anomaly-wind.ipynd
    │── explore.ipynd
    │── Data
        │── raw
            │── DSCVR
                │── dscovr_h0_mag_20220514_v01.cdf
            │── WIND
                │── wi_h1_swe_20220514_v01.cdf   
│── DST Index Prediction/            
│── README.md          # Project documentation
```

---
