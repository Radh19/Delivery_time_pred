# Order_Delivery_time_prediction

## 📌 Overview
This project aims to predict food delivery time based on factors like restaurant prep time, delivery distance, weather conditions, and traffic levels. The model uses Linear Regression to estimate delivery times and can help optimize food delivery operations.

## 📂 Dataset
The dataset is sourced from [Kaggle: Food Delivery Time Prediction](https://www.kaggle.com/datasets/denkuznetz/food-delivery-time-prediction?resource=download) and contains the following key features:

| Column Name            | Description |
|------------------------|-------------|
| `Prep_Time`           | Time taken by the restaurant to prepare the order (minutes) |
| `Delivery_Distance`   | Distance between restaurant and customer (km) |
| `Weather_Conditions`  | Weather status (Clear, Foggy, Rainy, etc.) |
| `Traffic_Conditions`  | Traffic status (Low, Medium, High) |
| `Vehicle_Type`        | Type of vehicle used for delivery (Bike, Scooter, etc.) |
| `Order_Time`          | Time of order placement (Morning, Afternoon, Evening) |
| `Delivery_Time` (Target) | Actual delivery time (minutes) |

---

## 🛠 Project Workflow
✔ **Step 1:** Load and Explore Dataset  
✔ **Step 2:** Data Preprocessing (handling missing values, encoding categorical variables)  
✔ **Step 3:** Exploratory Data Analysis (EDA) (correlation heatmaps, distributions)  
✔ **Step 4:** Train-Test Split (80% training, 20% testing)  
✔ **Step 5:** Model Training (Linear Regression)  
✔ **Step 6:** Model Evaluation (R² Score, MAE, MSE, RMSE)  
✔ **Step 7:** Prediction on Sample Orders  

---

## 📊 Model Performance

| Metric                         | Value  |
|--------------------------------|--------|
| **R² Score**                   | 0.76   |
| **Mean Absolute Error (MAE)**   | 7.28 min |
| **Mean Squared Error (MSE)**    | 109.24  |
| **Root Mean Squared Error (RMSE)** | 10.45 min |

✅ **The model performs well but could be improved using feature engineering or advanced models (Random Forest, XGBoost).**  

---

## 📝 Future Improvements

 🚀 **Hyperparameter tuning** using `GridSearchCV`  
🚀 **Feature Engineering** (Extracting new time-based or geographic features)  
🚀 **Try Advanced Models** (Random Forest, XGBoost, or Deep Learning)  
🚀 **Deploy as a Web App** using **Flask or Streamlit** 

---

## 📉 Visualizations

### **1️⃣ Actual vs Predicted Delivery Time**
A **scatter plot** comparing actual and predicted delivery times:

```python
import matplotlib.pyplot as plt

plt.figure(figsize=(8,6))
plt.scatter(y_test, y_pred, color='blue', alpha=0.5)
plt.plot([min(y_test), max(y_test)], [min(y_test), max(y_test)], linestyle='--', color='red', lw=2)  
plt.xlabel("Actual Delivery Time (minutes)")
plt.ylabel("Predicted Delivery Time (minutes)")
plt.title("Actual vs Predicted Delivery Time")
plt.grid(True)
plt.show()




