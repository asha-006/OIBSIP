# Car Price Prediction - Oasis Infobyte Data Science Internship (OIBSIP)

## 📌 1. Project Overview
Second-hand car pricing depends on various factors such as age, mileage, fuel type, and brand value. This project builds an end-to-end Machine Learning pipeline to accurately predict the resale price of used cars, helping buyers and sellers make data-driven decisions.

---

## 📂 2. Dataset Information
* **Source:** Oasis Infobyte Data Science Task 3 Dataset (`car data.csv`)
* **Target Variable:** `selling_price` (Price of the car in lakhs)
* **Key Features:** `name`, `year`, `selling_price`, `km_driven`, `fuel`, `seller_type`, `transmission`, `owner`

---

## 🛠️ 3. Step-by-Step Implementation Workflow

### **Step A: Data Loading & Inspection**
* Loaded the dataset using `pandas`.
* Inspected data types, missing values, and summary statistics to understand the data distribution.

### **Step B: Feature Engineering**
* **Brand Extraction:** Extracted the vehicle brand name from the raw `name` column and capitalized it.
* **Car Age Calculation:** Computed the age of the car dynamically (`Current Year - Manufacturing Year`) to capture depreciation value effectively.
* **Column Cleanup:** Dropped redundant original columns (`name`, `year`) to optimize the feature set.

### **Step C: Categorical Encoding**
* Converted categorical text variables (`fuel`, `seller_type`, `transmission`) into numerical format using **One-Hot Encoding** (`pd.get_dummies`) to make them compatible with machine learning algorithms.

### **Step D: Exploratory Data Analysis (EDA)**
* Visualized the distribution of selling prices using histograms.
* Analyzed price variations across fuel types and transmission modes using box plots and scatter plots.
* Generated a **Correlation Heatmap** to study the linear relationships between numerical features.

### **Step E: Model Training & Evaluation**
* Split the dataset into **80% Training** and **20% Testing** sets.
* Trained and evaluated two prominent regression models:
  1. **Linear Regression** (Baseline parametric model)
  2. **Random Forest Regressor** (Non-parametric ensemble model)
* **Performance Metrics Used:** 
  * Mean Absolute Error (MAE)
  * Root Mean Squared Error (RMSE)
  * $R^2$ Score (Coefficient of Determination)

---

## 📊 4. Key Findings & Insights
* **Random Forest Superiority:** The Random Forest Regressor outperformed Linear Regression by effectively capturing non-linear patterns and complex interactions among features.
* **Top Influencing Factors:** Feature importance analysis revealed that **Car Age**, initial market value, and **Transmission type** (Automatic vs Manual) have the highest impact on used car resale prices.

---

## 🏆 5. Conclusion
The machine learning pipeline was successfully implemented, evaluated, and verified. The Random Forest model provides reliable predictions, and this project can be further extended into a web application using **Flask** or **Streamlit** for real-time price estimation.