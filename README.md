# 🎓 Predictive Analysis: Impact of Educational Innovations on Crime Rates in Chicago  
![Python](https://img.shields.io/badge/Python-3.9-blue.svg) ![Project](https://img.shields.io/badge/Project-Completed-brightgreen)

🔍 **Predicting the long-term impact of school placement and after-school programs on neighborhood crime rates using supervised machine learning models.**

---

## 📌 Overview

This project explores the relationship between school establishment and crime rates in Chicago. Using spatial and temporal data, we trained predictive models to evaluate how school features and placement influence criminal activity over a seven-year period.

---

## 📊 Dataset Description

The datasets used in this project include:

- **School Data (2016-2023):**  
  - Types: Elementary, Middle, High, Preschool  
  - Features: Dress code, school hours, after-school duration, total students  
  - Location-based: Count of nearby schools within a 1 km radius

- **Crime Data (2001–2023):**  
  - Annual crime counts around schools (1 km radius)  
  - Geospatially aggregated  

Each school entry was paired with crime data for seven consecutive years.

---

## 🧹 Data Preparation

1. **Temporal Matching:**  
   - Paired 2016 school data with crime data from 2017 to 2023 to create 7 datasets (`df1` to `df7`)

2. **Feature Engineering:**  
   - One-hot encoding for school types  
   - Count of nearby schools by type  
   - Boolean flags for school categories  

3. **Target Variable:**  
   - `Crime_Count`: Number of crimes within 1 km radius of the school per year

---

## 🧪 Data Processing

- Cleaned missing values  
- Normalized numerical features  
- Encoded categorical data  
- Performed geospatial joins to relate schools and nearby crime zones  
- Created simulation inputs for testing new school placements

---

## 🤖 Models Used

Six regression models were trained on each dataset:

- 🌳 Random Forest Regressor  
- 💡 Gradient Boosting  
- ⚡ XGBoost  
- 🎯 SVM Regressor  
- 🚀 AdaBoost  
- 🏃‍♂️ SGDRegressor  

**Model Selection:**  
We retained the model with the lowest MAE and RMSE for each dataset.

| Dataset | Best Model        |
|---------|-------------------|
| df1     | Gradient Boosting |
| df2     | Gradient Boosting |
| df3     | SGDRegressor      |
| df4     | Gradient Boosting |
| df5     | Gradient Boosting |
| df6     | Gradient Boosting |
| df7     | SGDRegressor      |

---

## 📈 Evaluation

- 5-Fold cross-validation confirmed model generalization  
- Feature importance showed:
  - 📍 **Proximity to other schools** is more predictive than internal features like school hours or dress code  
  - ⏰ **After-school programs** had a measurable but minor influence

---

## 💡 Key Findings

- **School density** influences crime rate variation  
- **After-school duration** can slightly reduce crime  
- Internal school policies are less impactful than location-based variables

---

## 🧾 Results

### 1️⃣ Crime Prediction:
- Predict future crime (2024–2030) from 2023 school data

### 2️⃣ Impact Simulation:
- Simulate crime impact from adding a new school
- Analyze influence radius and impact on neighboring schools

🔧 **Example:**  
Adding a new school with ⏱️ 60-minute after-school time showed more crime reduction than one with just 20 minutes.

---

## 📌 Key Insights

- 📌 School presence and density are critical predictors of local crime  
- 📉 Extended after-school activities reduce crime slightly  
- 🧠 CRISP-DM methodology was essential in guiding the project from problem definition to evaluation

---

## 🧾 Conclusion

This study confirms a measurable but modest link between educational infrastructure and crime rates. While not the only factor, school presence—especially in dense clusters—can influence crime trends. Policymakers should use such predictive tools to guide urban education strategies and crime prevention.

---

## 👩‍💻 Authors

- Soumiya Razzouk  
- Chenjie Qian  
- Yann Legendre  
- Hicham Chekiri  

---

## 📂 Repository Structure

```bash
.
├── data/                # Raw dataset files
├── Notebook             # Jupyter notebook with modeling and analysis
├── Reports/             # Project technical reports and summaries
├── Articles/            # Scientific papers used to support hypotheses
└── README.md            # Readme 


