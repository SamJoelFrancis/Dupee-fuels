## 🔥 Dupree Fuels – Heating Oil Consumption Estimation
 
**Project**: Develop a regression-based model to estimate residential heating oil usage  
**Date**: June 13, 2024  



## 🚀 Project Objective

Dupree Fuels faces challenges in predicting oil consumption for 1,500+ customers due to:
- Unpredictable weather patterns
- Inefficient degree-day methods
- Over/underestimation causing unnecessary deliveries or fuel shortages

🔍 **Goal**: Build a **scalable, accurate, and interpretable** regression model using:
- Degree Days (weather-related heating need)
- Home Index (insulation, furnace type, size)
- Number of People (household size)

---

## 📊 Dataset Summary

**File**: `oil.csv`  
**Observations**: 40  
**Variables**:
- `Customer`: ID (int)
- `Oil.Usage`: Actual oil consumed (int)
- `Degree.Days`: Heating demand (int)
- `Home.Index`: Composite index for home characteristics (int)
- `Number.People`: Household size (int)

---

## 🧠 Model Comparisons

| Model   | Predictors                             | Adj. R² | Significant Variables     | Comments                             |
|---------|----------------------------------------|---------|----------------------------|--------------------------------------|
| Model 1 | All: Customer, Degree.Days, Home.Index, Number.People | 0.7662  | Degree.Days, Home.Index   | Risk of overfitting                  |
| Model 2 | Degree.Days, Home.Index, Number.People | 0.766   | Degree.Days, Home.Index   | Simpler but `Number.People` not sig |
| ✅ Model 3 | Degree.Days, Home.Index                  | **0.7708** | **Both significant**        | Best fit, most parsimonious          |

---

## 📈 Visualizations & Diagnostics

- Scatter plot: Oil Usage vs Degree Days
- ![image](https://github.com/user-attachments/assets/d104667b-348d-433b-bc8e-f798fab5c034)
- Bar chart: Oil Usage vs Home Index
- ![image](https://github.com/user-attachments/assets/d93dddcb-730c-4acb-85fd-40cb60d6c268)
- Scatter plot: Oil Usage vs Number of People
- ![image](https://github.com/user-attachments/assets/01393a5d-2e74-4ce0-92f8-d6d6ad00c737)
- Residual plots for all models to assess fit and homoscedasticity
![image](https://github.com/user-attachments/assets/e86f8291-2764-4806-9a60-8a3e15a8a054)
![image](https://github.com/user-attachments/assets/9cd534db-9273-4299-89e9-75d40e97e7f1)
![image](https://github.com/user-attachments/assets/6b540444-4a91-4237-adf7-b189a7915a8f)

---

## 📦 Libraries Used

```r
library(ggplot2)
library(leaps)
library(stargazer)

---

## Power Bi
-![image](https://github.com/user-attachments/assets/5b93458d-f956-407e-8234-07b92742a119)

