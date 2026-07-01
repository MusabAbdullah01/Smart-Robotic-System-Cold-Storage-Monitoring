# Smart Robotic System for Cold Storage Monitoring 🤖❄️
### Cognitive Robotics Project - Perception, Learning, and Action

---

## 📌 Project Overview
This project develops an AI-powered smart mobile robot system designed to automate environmental safety and quality monitoring within meat cold storage warehouses. Equipped with multi-sensory devices, the robot continuously tracks critical ambient parameters to detect hazardous anomalies and monitor worker activity patterns inside airtight freezing environments.

---

## 🚀 Key Features & Functionality
- **Multi-Sensor Data Fusion:** Collects and filters real-time streams of Temperature, Light, Sound, and $CO_2$ sensors.
- **Smart Alert System:** Automated heuristic logical engine that flags high/low temperature shifts (thawing risks) and carbon dioxide spike warnings.
- **Worker Presence Detection:** Implements a Supervised Machine Learning layer using a **Random Forest Classifier** to track human presence based on environmental changes.
- **Unsupervised Anomaly Detection:** Utilizes an **Isolation Forest** model to discover multi-variable micro-climatic fluctuations and system failures.
- **Cognitive Decision-Making Engine:** An integrated "Thinking Layer" that acts as the robot's brain, generating immediate situational deployment commands (e.g., Safe, Emergency Alert, Security Alert).

---

## 🛠️ Tech Stack & Tools
- **Language:** Python 🐍
- **Core Libraries:** Pandas, NumPy, Matplotlib
- **Machine Learning:** Scikit-Learn (Random Forest, Isolation Forest, StandardScaler)

---

## 📊 Performance & Insights

### 1. Feature Importance Analysis
According to the trained **Random Forest** model, environmental features have distinct impacts on worker detection:
- **Light Sensors (specifically `S1_Light`):** Hold the highest prediction weight, serving as a primary indicator of human entry.
- **$CO_2$ Slope & Sound:** Show significant contribution to the classification performance.
- **Temperature & PIR:** Have a lower relatively dynamic influence, showing that air quality and light are faster indicators of human presence than thermal shifts.

### 2. Analytical Metrics
- **Anomalies Detected:** 304 anomalous instances were successfully flagged using the **Isolation Forest** configuration ($Contamination = 3\%$).
- **Predictive Accuracy:** The Random Forest confusion matrix demonstrates excellent precision and recall boundaries for active worker tracking.

---

## 📂 Project Structure
```text
├── robotics_Project_code.ipynb  # Main Jupyter Notebook containing the full pipeline
└── README.md                    # Project documentation
