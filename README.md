#  Ship Crew Prediction using PySpark

##  Overview

This project is focused on predicting the **number of crew members** required for cruise ships based on various ship specifications such as tonnage, passenger capacity, age, length, cabins, and passenger density. The project uses **PySpark** for data processing and model building, making it scalable and efficient for large datasets.

The core objective is to develop a **regression model** that can estimate the required crew size, enabling cruise operators to plan better staffing strategies, improve operational efficiency, and reduce costs.

---

##  Objectives

- Load and transform ship data using **PySpark**.
- Prepare data for machine learning using **Spark ML library**.
- Train and evaluate a **Linear Regression model** to predict the number of crew members.
- Interpret results and extract actionable insights.
- Comparing results for different models.

---

##  Dataset Description

The dataset represents fictional cruise ship data with various operational and physical characteristics.

| Column              | Description                                      |
|---------------------|--------------------------------------------------|
| `Ship_name`         | Name of the cruise ship                          |
| `Cruise_line`       | Cruise line operator                             |
| `Age`               | Age of the ship in years                         |
| `Tonnage`           | Ship's weight capacity in tons                   |
| `Passengers`        | Number of passengers                             |
| `Length`            | Length of the ship in hundred meters             |
| `Cabins`            | Number of available cabins                       |
| `Passenger_density` | Ratio of passengers per tonnage                  |
| `Crew`              | Number of crew members (target variable)         |

**Target variable:** `Crew`

---

##  Tools & Technologies

- 🐍 Python 3.x  
- 🔥 Apache Spark (PySpark)  
- 📊 Spark ML library  
- 📁 Jupyter Notebooks  
- 💻 Google Colab for Spark setup  

---

## Data Preprocessing

- Dropped irrelevant columns (Ship_name).
- Categorical encoding of Cruise_line using StringIndexer.
- Combined features using VectorAssembler to create a single features column.

---

## Model Training & Evaluation

Used Regression models from PySpark’s ML library to predict the number of crew members

Models used: 
- LinearRegression
- RandomForestRegressor
- DecisionTreeRegressor
- GBTRegressor

Preformance Metrics: 
| Model             | R² Score | RMSE   | MAE    |
| ----------------- | -------- | ------ | ------ |
| Linear Regression | 0.8795   | 1.3554 | 0.7137 |
| Random Forest     | 0.8899   | 1.2957 | 0.4643 |
| Decision Tree     | 0.8890   | 1.3013 | 0.4955 |
| GBT Regressor     | 0.8872   | 1.3116 | 0.4674 |



