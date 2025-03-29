# 📦 Dynamic Reorder Point Optimization using Machine Learning

This project demonstrates how machine learning can optimize supply chain performance by dynamically predicting **reorder points** and **sales quantities** — replacing outdated static formulas with intelligent, data-driven forecasting.

---

## 🧠 Introduction

Supply chain and inventory management are among the most critical operations in any product-based business. One of the key challenges is determining **when and how much to reorder** to prevent stockouts or overstocking.

### 🏗️ The Problem with Traditional Methods

Traditional systems use static formulas like:

Reorder Point = Avg. Daily Demand × Lead Time + Safety Stock


While simple, these formulas assume constant demand and fixed lead time — which rarely reflect reality. As a result, businesses face:

- ❌ Frequent stockouts during seasonal spikes or promotions  
- ❌ Overstocking when demand drops  
- ❌ Poor response to disruptions and supplier delays  
- ❌ Excessive inventory holding costs  

---

### 🤖 Why Machine Learning?

Machine learning enables **dynamic forecasting** by learning patterns from historical data across multiple factors:

- ✅ Seasonality & trends  
- ✅ Promotions, pricing, and customer behavior  
- ✅ Store-level variability  
- ✅ Supplier lead times & stockouts  
- ✅ External market indicators  

ML models adapt continuously and can scale across thousands of SKUs and stores — transforming supply chain agility and efficiency.

---

## 📂 Repository Structure

| File                                                                 | Description |
|----------------------------------------------------------------------|-------------|
| `Dynamic_Reorder_Point_Optimization_Predicting_Reorder_Point.ipynb` | Predicts reorder points using features like Avg Demand, Lead Time, Safety Stock, Seasonality, etc. |
| `Dynamic_Reorder_Point_Optimization_Predicting_Sales_Quantity.ipynb`| Predicts real sales quantity based on seasonality, promotions, customer segments, etc. and compares ML vs traditional avg-based forecasting |

---

## ⚙️ Workflow Overview

### 1. 📊 Data Preparation
- Merged `demand_forecasting.csv` and `inventory_monitoring.csv`
- Engineered features: `Avg_Demand`, `Demand_Std`, `Safety Stock`, `IsWeekend`, etc.
- Encoded categorical variables and handled missing data

### 2. 📈 ML Model Training
- Models used:  
  - `RandomForestRegressor`  
  - `GradientBoostingRegressor`  
  - `LinearRegression`  
- Targets:
  - Reorder Point (based on traditional formula)
  - Sales Quantity (actual demand)

### 3. 🧪 Evaluation
- Metrics: `R² Score`, `RMSE`, `Absolute Error`
- Visuals: bar charts, error histograms, actual vs predicted plots
- Compared ML predictions to the traditional formula and average demand assumptions

---

## 📊 Results Summary

### 🔁 Reorder Point Prediction

| Model               | R² Score | RMSE | Notes |
|--------------------|----------|------|-------|
| Random Forest       | 0.87+     | ✅ Low | Best-performing model |
| Gradient Boosting   | 0.84+     | ✅ Low | Smooth predictions |
| Linear Regression   | ~0.6–0.7  | ⚠️ Higher RMSE | Too simplistic |


### 📦 Sales Quantity Prediction

| Model                  | R² Score | RMSE | Notes |
|-----------------------|----------|------|-------|
| Random Forest          | ✅ Best | ✅ Lowest | Captures demand dynamics |
| Gradient Boosting      | Good     | Low  | Competitive |
| Linear Regression      | ⚠️ Weak | High | Misses complexity |
| Traditional (Avg Demand) | ❌ Very low | High | Doesn’t adapt to change |

---

## 🌍 Supply Chain Impact

✔️ **Reduces Stockouts** by anticipating real-time demand  
✔️ **Prevents Overstocking** by adjusting reorder points dynamically  
✔️ **Improves Service Levels** and product availability  
✔️ **Decreases Holding Costs** and inventory waste  
✔️ **Supports Just-in-Time & Agile Supply Chains**  

---

## 🛠 Tools Used

- Python, Jupyter Notebook  
- Libraries: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`  
- Models: RandomForest, Gradient Boosting, Linear Regression  
- Input Files:  
  - `demand_forecasting.csv`  
  - `inventory_monitoring.csv`

## 📚 Data Source

The dataset used in this project was obtained from Kaggle:

**Inventory Optimization for Retail​​**  
Available at: [(https://www.kaggle.com/datasets/suvroo/inventory-optimization-for-retail?resource=download)]  
Licensed under: [MIT]


