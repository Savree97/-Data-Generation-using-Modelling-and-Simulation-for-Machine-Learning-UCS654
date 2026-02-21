# 🏥 Data Generation using Modelling & Simulation for Machine Learning  
### UCS654 – Assignment 6  
---

## 📌 Project Overview

This project demonstrates how modelling and simulation can be used to generate synthetic datasets for Machine Learning tasks.

A Hospital Queue System is simulated using SimPy, and the generated data is used to train and compare multiple regression models.

---

# 🚀 Simulation Tool Used

## 🧠 SimPy – Discrete Event Simulation Library

SimPy is a Python-based discrete-event simulation framework used to model real-world queue systems and resource-constrained environments.

---

# 🏥 Problem Description

A Hospital Patient Queue System is simulated where:

- Patients arrive randomly  
- Doctors are limited resources  
- Patients experience waiting time before service  

🎯 Goal:  
Predict **Average Waiting Time** using ML models based on system parameters.

---

# ⚙️ Simulation Parameters

| Parameter        | Lower Bound | Upper Bound |
|------------------|------------|-------------|
| arrival_rate     | 1          | 10          |
| service_rate     | 2          | 12          |
| doctors          | 1          | 5           |
| simulation_time  | 100        | Fixed       |

---

# 🔁 Data Generation

- Random parameter values generated within bounds  
- Simulation executed  
- Average waiting time recorded  
- Process repeated 1000 times  

Each simulation produces one dataset sample.

---

# 📂 Dataset

Features:

- arrival_rate  
- service_rate  
- doctors  
- avg_wait_time (target)  

Saved as:

```
simulation_data.csv
```

---

# 📈 Data Visualization

### 📊 Hospital Simulation Result

<p align="center">
  <img src="pink_plot.png" width="750">
</p>

---

# 🤖 Machine Learning Models Used

- Linear Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- SVR  
- KNN  

---

# 📏 Evaluation Metrics

- Mean Squared Error (MSE)  
- R² Score  

---

# 🏆 Results & Model Comparison

<p align="center">
  <img src="model_comparison.png" width="800">
</p>

### 🔍 Key Observations

- KNN achieved the lowest MSE and highest R² score  
- Random Forest and Gradient Boosting performed strongly  
- Linear Regression performed comparatively weaker  

---

# 📂 Repository Structure

```
Modelling_and_Simulation/
│
├── simpy_hospital_simulation.ipynb
├── simulation_data.csv
├── pink_plot.png
├── model_comparison.png
└── README.md
```

---

# ▶ How to Run

1. Open notebook in Google Colab  
2. Install SimPy:

```
pip install simpy
```

3. Run all cells  

---

# 👩‍💻 Author

Savree Dohar  
Roll No: 102317097  
UCS654 – Predictive Analytics & Statistics  
