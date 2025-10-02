# 🚗 Car Price Prediction using Machine Learning

This project predicts the **selling price of used cars** based on multiple features such as manufacturing year, fuel type, transmission type, and kilometers driven. The goal is to build regression models that accurately forecast car prices to help buyers and sellers make informed decisions.

---

## 🗂️ Dataset

**Columns:**
- `Car_Name` – Name of the car  
- `Year` – Year of manufacture  
- `Selling_Price` – Price at which car is sold (target variable)  
- `Present_Price` – Current ex-showroom price  
- `Kms_Driven` – Kilometers driven  
- `Fuel_Type` – Petrol / Diesel / CNG  
- `Seller_Type` – Dealer / Individual  
- `Transmission` – Manual / Automatic  
- `Owner` – Number of previous owners  

✅ **Preprocessing Steps**  
- Encoded categorical features (`Fuel_Type`, `Seller_Type`, `Transmission`)  
- Train-test split applied for evaluation  

---

## 🛠️ ML Techniques Used

- **Linear Regression**  
- **Lasso Regression**  
- **Decision Tree Regressor**  

---

## 📈 Model Performance

| Model               | R² Score | Mean Absolute Error |
|----------------------|----------|---------------------|
| Linear Regression    | 0.8498   | 1.118               |
| Lasso Regression     | 0.8709   | 1.051               |
| Decision Tree        | **0.9446** | **0.476**           |

The **Decision Tree Regressor** outperformed other models, achieving the highest accuracy.

---

## 📊 Key Visualizations

- Scatter plots of **Actual vs Predicted Prices** for all three models  
- Visual comparison of model performance  

---

## 🔮 Prediction on New Data

Example: Predicting the price of a **2015 model car**, with the following details:

Present Price: ₹7.5 Lakhs

Kms Driven: 25,000 km

Fuel Type: Petrol

Seller Type: Dealer

Transmission: Manual

Owner: 0 (First owner)

✅ The trained Decision Tree Regressor predicted the selling price for this car at approximately 5.8 Lakhs.
