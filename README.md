# Sales Forcasting Model for a Retail Company, Rossman Stores

## Project Overview
This project aims to address the inventory management challenges faced by a South America-based retail firm, Rossman Stores. Leveraging machine learning techniques, optimal inventory levels were predicted to balance demand and reduce wastage. The analysis utilized historical sales data to identify customer purchase patterns and forecast sales effectively.

## Dataset Description
- **Source**: Sakes data from Rossman Stores spanning 54 stores and 33 product types.
- **Period**: January 2013 to August 2017.
- **Features**:
  - `id`: Unique record identifier.
  - `date`: Date of the sales record.
  - `store_nbr`: Store number.
  - `product_type`: Type of the product.
  - `sales`: Total sales for a product.
  - `special_offer`: Intensity of promotional efforts (higher value = stronger promotion).

## Key Insights from Exploratory Data Analysis (EDA)
1. **Sales Patterns**:
   - Year-on-year growth in sales for most stores.
   - Grouped trends for stores suggest clustering opportunities.
   - High sales on weekends, with Thursdays being the lowest.
2. **Product Insights**:
   - Distinct sales trajectories for each product necessitated individual modeling.
   - Grocery and daily-use products contributed over 80% of total sales.
3. **Temporal Trends**:
   - High sales observed in December (festive season) and start of each month (salary-driven).
   - Sales dips were notable in January and mid-2015.

## Methodology
1. **Feature Engineering**:
   - Derived features like `dow` (day of the week), `lag_yoy_sales` (year-over-year lag), and `cluster` variables for better model performance.
   - Excluded outliers and inactive products for clean modeling.
2. **Modeling Techniques**:
   - Utilized **XGBoost Regressor**, **Random Forest**, and **LightGBM**.
   - Individual models created for each product type.
   - Hyperparameter tuning through custom GridSearch with cross-validation.
3. **Evaluation Metrics**:
   - **Negative Root Mean Squared Error (neg_RMSE)** for model selection.

## Results
- **Best Model**: XGBoost Regressor with `neg_RMSE = -46`.
- Predictions aligned closely with actual sales for most products.
- Outliers like seafood and books showed higher deviations, indicating areas for refinement.

## Challenges and Future Improvements
1. **Challenges**:
   - Sparse data for newly opened stores/products.
   - High variance in promotional effectiveness among products.
2. **Future Enhancements**:
   - Incorporate more lag-based features for better trend capture.
   - Develop dashboards for real-time monitoring.
   - Implement inter-store inventory redistribution.

## Repository Structure
- **`data/`**: Contains the cleaned and processed datasets.
- **`notebooks/`**: Jupyter notebooks with EDA, feature engineering, and modeling workflows

## Requirements
- Python 3.8+
- Libraries: `pandas`, `numpy`, `scikit-learn`, `xgboost`, `lightgbm`, `seaborn`, `matplotlib`, `plotly`

## How to Run
1. Clone the repository.
2. Install dependencies using `pip install -r requirements.txt`.
3. Navigate to `notebooks/` and run the Jupyter notebooks for EDA and modeling.
