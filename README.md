📚 Project Overview
# This project focuses on creating an efficient inventory management solution for a South American retail company, ABC. Leveraging machine learning, the goal was to predict sales trends across 33 product categories in 54 stores using historical data. A tailored XGBoost model was developed, achieving robust predictions and enabling better inventory decisions to minimize wastage and stockouts.

🚀 Key Features
Exploratory Data Analysis: Comprehensive analysis of sales trends by store, product, and day of the week to identify patterns and anomalies.
Feature Engineering: Added features like lag values, day-of-week trends, and sales clusters for improved model performance.
Machine Learning Models:
Utilized XGBoost, Random Forest, and LightGBM.
XGBoost achieved the best performance with an RMSE score of -46.
Custom Grid Search: Time-series-specific hyperparameter tuning for optimal model configuration.
Product-Specific Modeling: Individual models created for each product category to account for unique sales patterns.

🛠️ Tech Stack
Languages: Python
Libraries: Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn
Techniques: Time-series analysis, clustering, feature engineering

📊 Visual Insights
The analysis uncovered:
Weekend peaks and Thursday troughs in sales.
High sales contributions from five product categories, including Grocery and Beverages.

📂 Repository Contents
Code/: Contains scripts for data preprocessing, feature engineering, and modeling.
Reports/: Includes the detailed project report.
