# 🏥 Data Generation using Modelling & Simulation for Machine Learning  
### UCS654 – Assignment 6  
---

## 📌 Project Overview

In many real-world systems, collecting large-scale real data is expensive or impractical.  
Modelling and simulation provide an effective way to generate synthetic datasets for Machine Learning applications.

In this project, a **Hospital Queue System** is simulated using **SimPy**, and the generated dataset is used to train and evaluate multiple regression models.

---

# 🚀 Simulation Tool Used

## 🧠 SimPy – Discrete Event Simulation Library

SimPy is an open-source Python library used for modelling real-world systems such as:

- Queueing systems  
- Resource allocation  
- Service environments  

It integrates seamlessly with Machine Learning workflows.

---

# 🏥 Problem Description

A Hospital Patient Queue System is simulated where:

- Patients arrive randomly  
- Doctors are limited shared resources  
- Each patient experiences waiting time before treatment  

🎯 **Goal:**  
To analyze how system parameters influence **Average Waiting Time**, and train ML models to predict it.

---

# ⚙️ Simulation Parameters

| Parameter        | Lower Bound | Upper Bound |
|------------------|------------|-------------|
| arrival_rate     | 1          | 10          |
| service_rate     | 2          | 12          |
| doctors          | 1          | 5           |
| simulation_time  | 100        | Fixed       |

---

# 🔁 Data Generation Methodology

1️⃣ Random parameter values were generated within defined bounds  
2️⃣ Parameters were passed to the simulation  
3️⃣ The simulation was executed  
4️⃣ Average waiting time was recorded  
5️⃣ The process was repeated **1000 times**

Each simulation run produced one dataset sample.

---

# 📂 Dataset Description

The generated dataset contains:

- arrival_rate  
- service_rate  
- doctors  
- avg_wait_time (Target Variable)

The dataset is saved as:

```
Modelling_and_Simulation/simulation_data.csv
```

---

# 📈 Data Visualization

The scatter plot below shows the relationship between **arrival rate** and **average waiting time**.

Higher arrival rates generally lead to increased waiting times when system capacity becomes saturated.

### 📊 Hospital Simulation Result

<img src="Modelling_and_Simulation/pink_plot.png" width="750">

---

# 🤖 Machine Learning Models Used

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  
- Support Vector Regressor (SVR)  
- K-Nearest Neighbors Regressor (KNN)  

---

# 📏 Evaluation Metrics

- Mean Squared Error (MSE)  
- R² Score  

---

# 🏆 Results & Model Comparison

The performance comparison of all trained regression models is shown below:

| Rank | Model               | Mean Squared Error (MSE) | R² Score |
|------|---------------------|--------------------------|----------|
| 1️⃣  | K-Nearest Neighbors | 0.820175                 | 0.976906 |
| 2️⃣  | Random Forest       | 1.907055                 | 0.946302 |
| 3️⃣  | Gradient Boosting   | 2.511618                 | 0.929279 |
| 4️⃣  | Decision Tree       | 5.283305                 | 0.851234 |
| 5️⃣  | Support Vector Regr.| 23.523684                | 0.337626 |
| 6️⃣  | Linear Regression   | 26.723833                | 0.247517 |

---

### 🔍 Key Observations

- **K-Nearest Neighbors (KNN)** achieved the lowest MSE and highest R² score.
- Ensemble models such as **Random Forest** and **Gradient Boosting** performed strongly.
- Linear models showed comparatively weaker performance due to nonlinear system behavior.

---

# 🎯 Conclusion

This project demonstrates the effective integration of:

- Mathematical Modelling  
- Discrete-Event Simulation  
- Machine Learning  

Simulation-based data generation is particularly useful when real-world data is limited or expensive to collect.

---

# 📂 Repository Structure

```
README.md
Modelling_and_Simulation/
│
├── simpy_hospital_simulation.ipynb
├── simulation_data.csv
└── pink_plot.png
```

---

# 👩‍💻 Author

Savree Dohar  
Roll No: 102317097  
UCS654 – Predictive Analytics & Statistics  
