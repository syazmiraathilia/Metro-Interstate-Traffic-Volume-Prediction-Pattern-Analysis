# 🚗 Metro Interstate Traffic Volume Prediction & Pattern Analysis

## 📌 Project Overview
An end-to-end machine learning project designed to predict traffic volume and analyze traffic patterns for Smart City applications. This study compares four analytical approaches: **Supervised Learning, Unsupervised Learning, Association Rule Mining, and Deep Learning**, to generate actionable insights for intelligent transportation systems.

## 🛠️ Tech Stack & Tools
* **Programming Language:** R (RStudio)
* **Machine Learning:** Random Forest, Linear Regression, Multilayer Perceptron (MLP) Neural Network
* **Data Mining:** Apriori Association Rule Mining, K-Means Clustering
* **Visualization:** ggplot2

## 🔍 Methodology & Results
Data was preprocessed (handling missing values, feature engineering time-based variables) from a dataset of over 48,000 records. Four distinct models were built and evaluated:

1. **Supervised Learning (Random Forest vs. Linear Regression):**
   * The **Random Forest** model (500 trees) was the best performer, achieving an **R² of 0.93** (explaining 93% of the variance) and an RMSE of 545.74.
   * The Linear Regression baseline achieved a much lower R² of 0.20, proving traffic volume relies heavily on non-linear relationships.
2. **Deep Learning (Multilayer Perceptron):**
   * Built an MLP Neural Network with 24 input neurons and 5 hidden neurons, incorporating lag features for time-series forecasting. Achieved an **R² of 0.72**.
3. **Unsupervised Learning (K-Means Clustering):**
   * Utilized the Elbow Method to segment traffic into 3 distinct clusters, identifying patterns such as "High Traffic / Clear Weather" vs. "Low Traffic / Late Night".
4. **Association Rule Mining (Apriori):**
   * Generated rules (e.g., *If Weather=Clouds and Day=Sunday and Temp=Hot, then Traffic=Medium*) with high lift and confidence scores.

## 📊 Model Evaluation & Visualizations

**1. Random Forest Actual vs. Predicted & Residual Plot**
*Shows strong linear correlation, proving the model successfully captured traffic patterns.*
<img width="733" height="403" alt="Screenshot 2026-11-05 172339" src="https://github.com/user-attachments/assets/43bb0772-72c7-4ca6-8376-4c42e7593a63" />

**2. Variable Importance Analysis**
*Identified that temporal features (Hour, Day) were the strongest predictors of traffic volume, followed by temperature.*
<img width="511" height="292" alt="Screenshot 2026-11-05 172353" src="https://github.com/user-attachments/assets/71013706-08e5-4fc8-abce-cdbb38a3e49a" />

**3. Deep Learning (MLP) Architecture**
*Visualization of the Neural Network structure showing the input variables, hidden layers, and the predicted output.*
<img width="705" height="377" alt="Screenshot 2026-11-05 172419" src="https://github.com/user-attachments/assets/49364979-13ac-4011-9609-c14dd1ba642f" />

## 💡 Key Business Insights
* **Temporal factors rule traffic:** The Random Forest model proved that the hour of the day and the day of the week are far more important than weather conditions when predicting traffic volume.
* **Weather impact:** Medium traffic levels are highly associated with weekends, hot temperatures, and cloudy/clear skies (based on Apriori rules).
* **Model selection:** Ensemble methods (Random Forest) significantly outperform Deep Learning (MLP) and Linear Regression for this specific tabular time-series dataset.

---
*Note: The complete R code, dataset, and full academic report are available in this repository. (Future work includes deploying the best-performing model into an R Shiny application).*
