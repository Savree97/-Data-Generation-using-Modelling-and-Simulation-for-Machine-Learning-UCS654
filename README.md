# 🏥 Data Generation using Modelling & Simulation for Machine Learning  
### UCS654 – Assignment 6  
---

## 📌 Project Overview

In many real-world systems, collecting large-scale real data is expensive, slow, or sometimes impossible.  
Modelling and simulation provide a powerful alternative by generating **synthetic but realistic datasets**.

In this project, a **Hospital Queue System** is simulated using **SimPy**, and the generated data is used to train and compare multiple Machine Learning models.

This assignment demonstrates how simulation-based modelling can effectively support predictive analytics.

---

# 🚀 Simulation Tool Used

## 🧠 SimPy – Discrete Event Simulation Library

**SimPy** is an open-source Python library used for modelling real-world systems such as:

- Queueing systems  
- Resource allocation  
- Process scheduling  
- Service systems  

It is lightweight, efficient, and integrates seamlessly with ML workflows.

---

# 🏥 Problem Description

We simulate a **Hospital Patient Queue System** where:

- Patients arrive randomly  
- Doctors are limited resources  
- Each patient experiences waiting time before treatment  

🎯 **Goal:**  
To analyze how system parameters affect **Average Waiting Time**, and then train ML models to predict waiting time based on those parameters.

---

# ⚙️ Simulation Model & Parameters

## 🔄 Model Type
Discrete-event simulation using SimPy:

- Patient arrivals → Exponential distribution  
- Service time → Exponential distribution  
- Doctors → Limited shared resources  

---

## 📊 Parameter Bounds

| Parameter        | Description                         | Lower Bound | Upper Bound |
|------------------|-------------------------------------|-------------|-------------|
| arrival_rate     | Patient arrival rate                | 1           | 10          |
| service_rate     | Doctor service rate                 | 2           | 12          |
| doctors          | Number of available doctors         | 1           | 5           |
| simulation_time  | Total simulation duration           | 100         | Fixed       |

These bounds ensure realistic system behavior while maintaining stability.

---

# 🔁 Data Generation Methodology

The following steps were executed:

1️⃣ Random parameter values were generated within defined bounds  
2️⃣ Parameters were passed to the SimPy simulation  
3️⃣ The simulation ran for fixed duration  
4️⃣ Average waiting time was recorded  
5️⃣ Process repeated **1000 times**

Each simulation run produces one dataset sample.

---

# 📂 Dataset Description

The generated dataset contains:

| Feature Name     | Description |
|------------------|------------|
| arrival_rate     | Patient arrival rate |
| service_rate     | Doctor service rate |
| doctors          | Number of doctors |
| avg_wait_time    | Average patient waiting time (Target Variable) |

The dataset is stored as:

simulation_data.csv

---

# 📈 Data Visualization

The following scatter plot visualizes the relationship between **arrival rate** and **average waiting time**.

Higher arrival rates generally lead to increased waiting times when system capacity becomes saturated.

### 📊 Hospital Simulation Result

![Hospital Simulation Result](pink_plot.png)

*(Make sure your pink scatter plot image is saved in the repository as `pink_plot.png`.)*

---

# 🤖 Machine Learning Models Used

The following regression models were trained:

1️⃣ Linear Regression  
2️⃣ Decision Tree Regressor  
3️⃣ Random Forest Regressor  
4️⃣ Gradient Boosting Regressor  
5️⃣ Support Vector Regressor (SVR)  
6️⃣ K-Nearest Neighbors Regressor (KNN)  

---

# 📏 Model Evaluation Metrics

Models were evaluated using:

- 📉 **Mean Squared Error (MSE)**
- 📊 **R² Score**

These metrics allow accurate performance comparison across models.

---

# 🏆 Results & Model Comparison

A comparison table was generated for all models.

📌 Observation:

- Tree-based ensemble models like **Random Forest** and **Gradient Boosting** achieved the best performance.
- They captured nonlinear relationships better than linear models.

(Add your comparison table screenshot here if required.)

---

# 🧠 Key Insights

✔ Simulation successfully generated meaningful synthetic data  
✔ System behavior matches queue theory expectations  
✔ ML models effectively learned system patterns  
✔ Ensemble methods outperform simpler regression techniques  

---

# 🎯 Conclusion

This project demonstrates the powerful synergy between:

- 🧮 Mathematical Modelling  
- 🔄 Simulation  
- 🤖 Machine Learning  

Simulation-based data generation is highly valuable when:

- Real-world data is scarce  
- Data collection is expensive  
- Controlled experimentation is required  

The integration of SimPy with ML provides a scalable framework for predictive modeling.

---

# 📂 Repository Structure

simpy_hospital_simulation.ipynb  
simulation_data.csv  
README.md  
pink_plot.png  

---

# ▶ How to Run

1. Open the notebook in Google Colab  
2. Install SimPy using:

pip install simpy  

3. Run all cells sequentially  
4. Observe simulation results, plots, and ML comparison  

---

# ✨ Technologies Used

- Python  
- SimPy  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  

---

# 👩‍💻 Author

**Savree Dohar**  
Roll No: 102317097  
UCS654 – Predictive Analytics & Statistics  
