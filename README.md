# Business Sales ML System

## Project Overview

This project is an **end-to-end Machine Learning system** built using real-world sales data.
It predicts key business outcomes and helps in decision-making using data-driven insights.

---

## Objectives

* 📈 Predict **Sales Revenue**
* 🎯 Predict **Order Status (Shipped / Not Shipped)**
* 🛒 Predict **Product Demand (Quantity Ordered)**

---

## Dataset

The dataset contains ~2800+ sales records with features like:

* QUANTITYORDERED
* PRICEEACH
* SALES
* STATUS
* PRODUCTLINE
* COUNTRY
* DEALSIZE
* MONTH, YEAR

---

## Workflow

### Data Preprocessing

* Handled missing values
* Converted categorical features using **Label Encoding**
* Ensured all features are numeric

---

### Feature Engineering

* `TOTAL_PRICE = QUANTITY × PRICE`
* `PRICE_DIFF = MSRP - PRICEEACH`

These features improved model performance significantly.

---

 Model 1: Sales Prediction

* Model: **Random Forest Regressor**
* Performance:

  * R² Score ≈ **0.89**
  * MAE ≈ **326**

✔ Strong and reliable model
✔ Captures real-world pricing variations

---

## Model 2: Status Prediction

* Converted to **Binary Classification** due to imbalance
* Model: **Random Forest Classifier**
* Performance:

  * Accuracy ≈ **0.96**
  * Good precision & recall balance

✔ Handles class imbalance using `class_weight='balanced'`
✔ Predicts successful vs risky orders

---

## Model 3: Demand Prediction

* Target: `QUANTITYORDERED`
* Model: **Random Forest Regressor**
* Performance:

  * R² Score ≈ **0.45**

✔ Moderate performance
✔ Reflects real-world uncertainty in demand

---

## Visualizations

* Actual vs Predicted Graphs
* Confusion Matrix
* Error Distribution

---

## Challenges

* Severe class imbalance in STATUS
* Weak feature relationships for demand
* Real-world noisy data

---

## Key Learnings

* Feature Engineering > Model Selection
* Real-world data is imperfect
* Evaluation metrics matter more than accuracy
* Not all problems are perfectly predictable

---

## Future Improvements

* Use XGBoost / LightGBM
* Hyperparameter tuning
* Build Streamlit UI
* Apply time-series forecasting for demand

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* Matplotlib, Seaborn

---

## Sample Prediction

**Input:**

* Quantity: 30
* Price: 100
* Month: 5
* Year: 2004

**Output:**

* Sales ≈ 2875
* Status → Shipped
* Demand → ~Predicted Quantity

---


---

## Conclusion

This project demonstrates a complete **end-to-end ML pipeline**, showcasing real-world problem-solving using data science techniques.

---
